---
title: Gyakori kérdések (GYIK)
description: Gyakori kérdések az Azure PowerShell-lel kapcsolatban.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407510"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Gyakori kérdések az Azure PowerShell-lel kapcsolatban

## <a name="what-is-azure-powershell"></a>Mi az az Azure PowerShell?

Az Azure PowerShell olyan parancsmagok készletét kínálja, amelyekkel az Azure-erőforrások közvetlenül a PowerShell-lel kezelhetők. 2018 decemberében az Az PowerShell-modul általánosan elérhetővé vált. Ma már ez az Azure használatához ajánlott PowerShell-modul. Ha többet is meg szeretne tudni az Az PowerShell-modulról, olvassa el [az Azure PowerShell új Az moduljának ismertetését](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Hogyan tilthatom le a kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzeneteket az Azure PowerShellben?

Az Azure PowerShell kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzeneteinek letiltásához állítsa a `SuppressAzurePowerShellBreakingChangeWarnings` környezeti változót `true` értékre.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
