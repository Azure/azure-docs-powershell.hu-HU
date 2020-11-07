---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
ms.openlocfilehash: 604eec977e8cb821986e3dcc0690fa4dfb65b526
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839974"
---
# <span data-ttu-id="00a86-101">Get-AzWebAppMetric</span><span class="sxs-lookup"><span data-stu-id="00a86-101">Get-AzWebAppMetric</span></span>

## <span data-ttu-id="00a86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00a86-102">SYNOPSIS</span></span>
<span data-ttu-id="00a86-103">Azure Web App metrikáit kapja.</span><span class="sxs-lookup"><span data-stu-id="00a86-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="00a86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00a86-104">SYNTAX</span></span>

### <span data-ttu-id="00a86-105">S1</span><span class="sxs-lookup"><span data-stu-id="00a86-105">S1</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00a86-106">S2</span><span class="sxs-lookup"><span data-stu-id="00a86-106">S2</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00a86-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="00a86-107">DESCRIPTION</span></span>
<span data-ttu-id="00a86-108">A **Get-AzWebAppMetric** webalkalmazás metrikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="00a86-108">The **Get-AzWebAppMetric** gets Web App metrics.</span></span>

## <span data-ttu-id="00a86-109">Példák</span><span class="sxs-lookup"><span data-stu-id="00a86-109">EXAMPLES</span></span>

### <span data-ttu-id="00a86-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="00a86-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="00a86-111">Ez a parancs a Web App ContosoWebApp percenkénti kérelmeket kapja meg (PT1M-szavazási idő 1 perc) a kezdési időpont és a befejezési időpont között</span><span class="sxs-lookup"><span data-stu-id="00a86-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="00a86-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00a86-112">PARAMETERS</span></span>

### <span data-ttu-id="00a86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a86-113">-DefaultProfile</span></span>
<span data-ttu-id="00a86-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00a86-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00a86-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="00a86-115">-EndTime</span></span>
<span data-ttu-id="00a86-116">Befejezési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="00a86-116">End Time in UTC</span></span>

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

### <span data-ttu-id="00a86-117">-Részletesség</span><span class="sxs-lookup"><span data-stu-id="00a86-117">-Granularity</span></span>
<span data-ttu-id="00a86-118">Granularitása</span><span class="sxs-lookup"><span data-stu-id="00a86-118">Granularity</span></span>

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

### <span data-ttu-id="00a86-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="00a86-119">-InstanceDetails</span></span>
<span data-ttu-id="00a86-120">Példány részletei</span><span class="sxs-lookup"><span data-stu-id="00a86-120">Instance Details</span></span>

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

### <span data-ttu-id="00a86-121">-Metrikák</span><span class="sxs-lookup"><span data-stu-id="00a86-121">-Metrics</span></span>
<span data-ttu-id="00a86-122">Metrikák karakterlánc-tömbként</span><span class="sxs-lookup"><span data-stu-id="00a86-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="00a86-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="00a86-123">-Name</span></span>
<span data-ttu-id="00a86-124">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="00a86-124">WebApp Name</span></span>

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

### <span data-ttu-id="00a86-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00a86-125">-ResourceGroupName</span></span>
<span data-ttu-id="00a86-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="00a86-126">Resource Group Name</span></span>

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

### <span data-ttu-id="00a86-127">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="00a86-127">-StartTime</span></span>
<span data-ttu-id="00a86-128">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="00a86-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="00a86-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="00a86-129">-WebApp</span></span>
<span data-ttu-id="00a86-130">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="00a86-130">WebApp object</span></span>

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

### <span data-ttu-id="00a86-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a86-131">CommonParameters</span></span>
<span data-ttu-id="00a86-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00a86-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a86-133">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="00a86-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a86-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00a86-134">INPUTS</span></span>

### <span data-ttu-id="00a86-135">System. String</span><span class="sxs-lookup"><span data-stu-id="00a86-135">System.String</span></span>

### <span data-ttu-id="00a86-136">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="00a86-136">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="00a86-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00a86-137">OUTPUTS</span></span>

### <span data-ttu-id="00a86-138">Microsoft. Azure. Management. WebSites. models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="00a86-138">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="00a86-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00a86-139">NOTES</span></span>

## <span data-ttu-id="00a86-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00a86-140">RELATED LINKS</span></span>

[<span data-ttu-id="00a86-141">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="00a86-141">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

