<!--
* Copyright (c) 2017, 2022 IBM Corp. and others
*
* This program and the accompanying materials are made
* available under the terms of the Eclipse Public License 2.0
* which accompanies this distribution and is available at
* https://www.eclipse.org/legal/epl-2.0/ or the Apache
* License, Version 2.0 which accompanies this distribution and
* is available at https://www.apache.org/licenses/LICENSE-2.0.
*
* This Source Code may also be made available under the
* following Secondary Licenses when the conditions for such
* availability set forth in the Eclipse Public License, v. 2.0
* are satisfied: GNU General Public License, version 2 with
* the GNU Classpath Exception [1] and GNU General Public
* License, version 2 with the OpenJDK Assembly Exception [2].
*
* [1] https://www.gnu.org/software/classpath/license.html
* [2] http://openjdk.java.net/legal/assembly-exception.html
*
* SPDX-License-Identifier: EPL-2.0 OR Apache-2.0 OR GPL-2.0 WITH
* Classpath-exception-2.0 OR LicenseRef-GPL-2.0 WITH Assembly-exception
-->

# ‑Xenableexcessivegc / ‑Xdisableexcessivegc

Enables or disables the throwing of an `OutOfMemory` exception if excessive time is spent in the GC.

If excessive time is spent in the GC, the option returns `null` for an allocate request and thus causes an `OutOfMemory` exception to be thrown.

:fontawesome-solid-pencil-alt:{: .note aria-hidden="true"} **Note:** The `OutOfMemory` exception is thrown only when the heap has been fully expanded and the percentage of application run time that is not spent in garbage collection is at least 95%. This percentage is the default value that triggers an excessive GC event. You can control this value with the [`-Xgc:excessiveGCratio`](xgc.md#excessivegcratio) option.

## Syntax

| Setting               | Effect            | Default                                                                            |
|-----------------------|-------------------|:----------------------------------------------------------------------------------:|
|`-Xenableexcessivegc`  | Enable exception  | :fontawesome-solid-check:{: .yes aria-hidden="true"}<span class="sr-only">yes</span>     |
|`-Xdisableexcessivegc` | Disable exception |                                                                                    |

These options can be used with all OpenJ9 GC policies.

<!-- ==== END OF TOPIC ==== xenableexcessivegc.md ==== -->
<!-- ==== END OF TOPIC ==== xdisableexcessivegc.md ==== -->
