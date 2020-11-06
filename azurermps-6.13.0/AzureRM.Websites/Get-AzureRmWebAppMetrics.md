---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
ms.openlocfilehash: 47fa876ff021dd920627ce4f08089c5fd04fb885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494850"
---
# <span data-ttu-id="68512-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="68512-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="68512-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68512-102">SYNOPSIS</span></span>
<span data-ttu-id="68512-103">Azure Web App metrikáit kapja.</span><span class="sxs-lookup"><span data-stu-id="68512-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68512-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68512-104">SYNTAX</span></span>

### <span data-ttu-id="68512-105">S1</span><span class="sxs-lookup"><span data-stu-id="68512-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68512-106">S2</span><span class="sxs-lookup"><span data-stu-id="68512-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68512-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="68512-107">DESCRIPTION</span></span>
<span data-ttu-id="68512-108">A **Get-AzureRmWebAppMetrics** webalkalmazás metrikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="68512-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="68512-109">Példák</span><span class="sxs-lookup"><span data-stu-id="68512-109">EXAMPLES</span></span>

### <span data-ttu-id="68512-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="68512-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="68512-111">Ez a parancs a Web App ContosoWebApp percenkénti kérelmeket kapja meg (PT1M-szavazási idő 1 perc) a kezdési időpont és a befejezési időpont között</span><span class="sxs-lookup"><span data-stu-id="68512-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="68512-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68512-112">PARAMETERS</span></span>

### <span data-ttu-id="68512-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68512-113">-DefaultProfile</span></span>
<span data-ttu-id="68512-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68512-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68512-115">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="68512-115">-EndTime</span></span>
<span data-ttu-id="68512-116">Befejezési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="68512-116">End Time in UTC</span></span>

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

### <span data-ttu-id="68512-117">-Részletesség</span><span class="sxs-lookup"><span data-stu-id="68512-117">-Granularity</span></span>
<span data-ttu-id="68512-118">Granularitása</span><span class="sxs-lookup"><span data-stu-id="68512-118">Granularity</span></span>

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

### <span data-ttu-id="68512-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="68512-119">-InstanceDetails</span></span>
<span data-ttu-id="68512-120">Példány részletei</span><span class="sxs-lookup"><span data-stu-id="68512-120">Instance Details</span></span>

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

### <span data-ttu-id="68512-121">-Metrikák</span><span class="sxs-lookup"><span data-stu-id="68512-121">-Metrics</span></span>
<span data-ttu-id="68512-122">Metrikák karakterlánc-tömbként</span><span class="sxs-lookup"><span data-stu-id="68512-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="68512-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68512-123">-Name</span></span>
<span data-ttu-id="68512-124">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="68512-124">WebApp Name</span></span>

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

### <span data-ttu-id="68512-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68512-125">-ResourceGroupName</span></span>
<span data-ttu-id="68512-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="68512-126">Resource Group Name</span></span>

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

### <span data-ttu-id="68512-127">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="68512-127">-StartTime</span></span>
<span data-ttu-id="68512-128">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="68512-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="68512-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="68512-129">-WebApp</span></span>
<span data-ttu-id="68512-130">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="68512-130">WebApp object</span></span>

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

### <span data-ttu-id="68512-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68512-131">CommonParameters</span></span>
<span data-ttu-id="68512-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68512-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68512-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68512-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68512-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68512-134">INPUTS</span></span>

### <span data-ttu-id="68512-135">System. String</span><span class="sxs-lookup"><span data-stu-id="68512-135">System.String</span></span>

### <span data-ttu-id="68512-136">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="68512-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="68512-137">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="68512-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="68512-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68512-138">OUTPUTS</span></span>

### <span data-ttu-id="68512-139">Microsoft. Azure. Management. WebSites. models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="68512-139">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="68512-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68512-140">NOTES</span></span>

## <span data-ttu-id="68512-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68512-141">RELATED LINKS</span></span>

[<span data-ttu-id="68512-142">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="68512-142">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

