---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193985"
---
# <span data-ttu-id="0b4bf-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="0b4bf-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="0b4bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b4bf-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4bf-103">Az Azure PowerShell-parancsmagok fejlesztésére az adatok gyűjtésének kijavítása.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="0b4bf-104">Az adatokat alapértelmezés szerint gyűjtjük, hacsak nem kifejezetten kikapcsolja.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="0b4bf-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b4bf-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b4bf-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b4bf-106">DESCRIPTION</span></span>

<span data-ttu-id="0b4bf-107">A `Disable-AzDataCollection` parancsmag az adatgyűjtési szolgáltatás kikapcsolásához használható.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="0b4bf-108">Az Azure PowerShell alapértelmezés szerint automatikusan gyűjti a telemetriai adatokat.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="0b4bf-109">Az adatgyűjtés letiltásához explicit módon le kell jelentkeznie. A Microsoft összesíti az összegyűjtött adatokat a használati minták meghatározására, a gyakori problémák felismerésére, valamint az Azure PowerShell használatának javítására.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="0b4bf-110">A Microsoft Azure PowerShell nem gyűjt semmilyen személyes vagy személyes adatot.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="0b4bf-111">Ha korábban kikapcsolta a rendszert, futtassa a `Enable-AzDataCollection` parancsmagot, és engedélyezze újra a jelenlegi felhasználó adatgyűjtését az aktuális gépen.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="0b4bf-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0b4bf-112">EXAMPLES</span></span>

### <span data-ttu-id="0b4bf-113">1. példa: az aktuális felhasználó adatgyűjtésének letiltása</span><span class="sxs-lookup"><span data-stu-id="0b4bf-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="0b4bf-114">Az alábbi példa azt szemlélteti, hogy miként tilthatja le az aktuális felhasználó adatgyűjtését.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="0b4bf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b4bf-115">PARAMETERS</span></span>

### <span data-ttu-id="0b4bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4bf-116">-DefaultProfile</span></span>

<span data-ttu-id="0b4bf-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4bf-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0b4bf-118">-Confirm</span></span>

<span data-ttu-id="0b4bf-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4bf-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b4bf-120">-WhatIf</span></span>

<span data-ttu-id="0b4bf-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b4bf-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b4bf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4bf-123">CommonParameters</span></span>

<span data-ttu-id="0b4bf-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b4bf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4bf-125">További információt a [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0b4bf-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="0b4bf-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b4bf-126">INPUTS</span></span>

### <span data-ttu-id="0b4bf-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="0b4bf-127">None</span></span>

## <span data-ttu-id="0b4bf-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b4bf-128">OUTPUTS</span></span>

### <span data-ttu-id="0b4bf-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="0b4bf-129">System.Void</span></span>

## <span data-ttu-id="0b4bf-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b4bf-130">NOTES</span></span>

## <span data-ttu-id="0b4bf-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b4bf-131">RELATED LINKS</span></span>

[<span data-ttu-id="0b4bf-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="0b4bf-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)