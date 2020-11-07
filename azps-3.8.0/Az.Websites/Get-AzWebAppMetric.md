---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
ms.openlocfilehash: 91b5de48805e458b771227ca9c92e9891be170e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845745"
---
# <span data-ttu-id="cc421-101">Get-AzWebAppMetric</span><span class="sxs-lookup"><span data-stu-id="cc421-101">Get-AzWebAppMetric</span></span>

## <span data-ttu-id="cc421-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc421-102">SYNOPSIS</span></span>
<span data-ttu-id="cc421-103">Azure Web App metrikáit kapja.</span><span class="sxs-lookup"><span data-stu-id="cc421-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="cc421-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc421-104">SYNTAX</span></span>

### <span data-ttu-id="cc421-105">S1</span><span class="sxs-lookup"><span data-stu-id="cc421-105">S1</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc421-106">S2</span><span class="sxs-lookup"><span data-stu-id="cc421-106">S2</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc421-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc421-107">DESCRIPTION</span></span>
<span data-ttu-id="cc421-108">A **Get-AzWebAppMetric** webalkalmazás metrikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="cc421-108">The **Get-AzWebAppMetric** gets Web App metrics.</span></span>

## <span data-ttu-id="cc421-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cc421-109">EXAMPLES</span></span>

### <span data-ttu-id="cc421-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cc421-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="cc421-111">Ez a parancs a Web App ContosoWebApp percenkénti kérelmeket kapja meg (PT1M-szavazási idő 1 perc) a kezdési időpont és a befejezési időpont között</span><span class="sxs-lookup"><span data-stu-id="cc421-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="cc421-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc421-112">PARAMETERS</span></span>

### <span data-ttu-id="cc421-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc421-113">-DefaultProfile</span></span>
<span data-ttu-id="cc421-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc421-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc421-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="cc421-115">-EndTime</span></span>
<span data-ttu-id="cc421-116">Befejezési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="cc421-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc421-117">-Részletesség</span><span class="sxs-lookup"><span data-stu-id="cc421-117">-Granularity</span></span>
<span data-ttu-id="cc421-118">Granularitása</span><span class="sxs-lookup"><span data-stu-id="cc421-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc421-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="cc421-119">-InstanceDetails</span></span>
<span data-ttu-id="cc421-120">Példány részletei</span><span class="sxs-lookup"><span data-stu-id="cc421-120">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc421-121">-Metrikák</span><span class="sxs-lookup"><span data-stu-id="cc421-121">-Metrics</span></span>
<span data-ttu-id="cc421-122">Metrikák karakterlánc-tömbként</span><span class="sxs-lookup"><span data-stu-id="cc421-122">Metrics as a string array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc421-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc421-123">-Name</span></span>
<span data-ttu-id="cc421-124">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="cc421-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc421-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc421-125">-ResourceGroupName</span></span>
<span data-ttu-id="cc421-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="cc421-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc421-127">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="cc421-127">-StartTime</span></span>
<span data-ttu-id="cc421-128">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="cc421-128">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc421-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cc421-129">-WebApp</span></span>
<span data-ttu-id="cc421-130">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="cc421-130">WebApp object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc421-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc421-131">CommonParameters</span></span>
<span data-ttu-id="cc421-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc421-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc421-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cc421-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc421-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc421-134">INPUTS</span></span>

### <span data-ttu-id="cc421-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cc421-135">System.String</span></span>

### <span data-ttu-id="cc421-136">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="cc421-136">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cc421-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc421-137">OUTPUTS</span></span>

### <span data-ttu-id="cc421-138">Microsoft. Azure. Management. WebSites. models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="cc421-138">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="cc421-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc421-139">NOTES</span></span>

## <span data-ttu-id="cc421-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc421-140">RELATED LINKS</span></span>

[<span data-ttu-id="cc421-141">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="cc421-141">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

