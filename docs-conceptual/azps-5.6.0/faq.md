---
title: Gyakori kérdések (GYIK)
description: Gyakori kérdések az Azure PowerShell-lel kapcsolatban.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101881910"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Gyakori kérdések az Azure PowerShell-lel kapcsolatban

## <a name="what-is-azure-powershell"></a>Mi az az Azure PowerShell?

Az Azure PowerShell olyan parancsmagok készletét kínálja, amelyekkel az Azure-erőforrások közvetlenül a PowerShell-lel kezelhetők. 2018 decemberében az Az PowerShell-modul általánosan elérhetővé vált. Ma már ez az Azure használatához ajánlott PowerShell-modul. Ha többet is meg szeretne tudni az Az PowerShell-modulról, olvassa el [az Azure PowerShell új Az moduljának ismertetését](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Hogyan tilthatom le a kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzeneteket az Azure PowerShellben?

Az Azure PowerShell kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzeneteinek letiltásához állítsa a `SuppressAzurePowerShellBreakingChangeWarnings` környezeti változót `true` értékre.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
