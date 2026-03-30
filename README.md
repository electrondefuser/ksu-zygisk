# 👁️ Envisioned
**The Zygote Injection Module**

> *"A crude fusion of Sokolov’s alchemy and the Void's influence, designed to rewrite a process's intent before it is even born."*

**Zygis** is a ritualistic injection module, channeled through the [`ptrace`](https://man7.org/linux/man-pages/man2/ptrace.2.html) tether. It manifests Zygisk API stability for the heretical Kernels of **APatch** and **KernelSU**, serving as a superior replacement for the crude machinations of standard Magisk.

---

## Core Tenets

The Envisioned module is forged upon four immutable pillars:

* **Sacred Alignment:** Maintains total synchronization with [Magisk’s Zygisk API](https://github.com/topjohnwu/Magisk/tree/master/native/src/core/zygisk). The blueprints are etched within the [injector](https://github.com/JingMatrix/NeoZygisk/tree/master/loader/src/injector) for those who seek to study the design.
* **Brutalist Efficiency:** A lean, unyielding implementation. No bloat, no excess—only the cold precision of an Overseer’s blade to ensure the stability of the Great Design.
* **Ethereal Dissipation:** Once the ritual concludes and modules are unlinked, Zygis guarantees the total erasure of its presence. No echoes remain in the mind of the process.
* **The Veil (DenyList):** Employs a sophisticated shroud to grant granular control over what the Empire sees. Hide your marks; walk through the Grand Palace as a ghost.

---

## The DenyList: Bending Reality

Modern root solutions rely on shifting [mounts](https://man7.org/linux/man-pages/man8/mount.8.html)—overlays of reality that do not truly exist in the system partitions. The DenyList is your Outsider’s Mark, allowing you to manipulate [mount namespaces](https://man7.org/linux/man-pages/man7/mount_namespaces.7.html) so each application perceives only the reality you permit.

| Subject State | Perception of the World | Strategic Intent |
| :--- | :--- | :--- |
| **Granted the Mark** | Full Access + Module Overlays | For trusted agents requiring total dominion over the system’s architecture. |
| **Envisioned (DenyList)** | Pristine, Unmodified Reality | A "clean" environment for prying eyes. Root detection is blinded; the world appears as if the Abbey still held total control. |

### Strategies of Concealment

To achieve a "Clean Slate" for those on the DenyList, Zygis utilizes two distinct rites:

1.  **The Zygote Purge (Primary Rite)**
    An experimental technique to bypass the most vigilant Watchers. Zygis attempts to unmount all traces of the Mark directly from the Zygote process itself—cleansing the blood *before* the process is even born. If a module is deemed critical to system life (e.g., an overlay in `/product`), the rite is aborted to prevent a total collapse of the Zygote.
2.  **The Void Switch (Fallback Rite)**
    Should the Purge be deemed unsafe, Zygis reverts to the standard path. As a process forks, we use the `setns` incantation to cast it into a cached, untainted namespace—isolating it entirely from our modifications.

---

## Configuration

To shroud an application from the Empire’s gaze, adjust the settings within your chosen management vessel:

* **APatch / KernelSU:** Invoke the **`Umount modules`** command for your target.
* **Magisk:** Navigate to the **`Configure DenyList`** scrolls.

> [!CAUTION]
> **A Warning to Magisk Users**
> The **`Enforce DenyList`** toggle within Magisk activates its own, inferior shroud. This may conflict with the Envisioned’s superior masking techniques. For a perfect shadow, leave Magisk’s enforcement disabled and trust solely in the Zygis module.
