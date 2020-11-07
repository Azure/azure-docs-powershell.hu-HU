---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
ms.openlocfilehash: 00e8814c72f0e9d52fae2504a41bef3e8e94e7ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673070"
---
# <span data-ttu-id="fbc5f-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="fbc5f-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="fbc5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc5f-103">Azure Web App metrikáit kapja.</span><span class="sxs-lookup"><span data-stu-id="fbc5f-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbc5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbc5f-104">SYNTAX</span></span>

### <span data-ttu-id="fbc5f-105">S1</span><span class="sxs-lookup"><span data-stu-id="fbc5f-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbc5f-106">S2</span><span class="sxs-lookup"><span data-stu-id="fbc5f-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbc5f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbc5f-107">DESCRIPTION</span></span>
<span data-ttu-id="fbc5f-108">A **Get-AzureRmWebAppMetrics** webalkalmazás metrikáját kapja.</span><span class="sxs-lookup"><span data-stu-id="fbc5f-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="fbc5f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fbc5f-109">EXAMPLES</span></span>

### <span data-ttu-id="fbc5f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fbc5f-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="fbc5f-111">Ez a parancs a Web App ContosoWebApp percenkénti kérelmeket kapja meg (PT1M-szavazási idő 1 perc) a kezdési időpont és a befejezési időpont között</span><span class="sxs-lookup"><span data-stu-id="fbc5f-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="fbc5f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbc5f-112">PARAMETERS</span></span>

### <span data-ttu-id="fbc5f-113">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="fbc5f-113">-EndTime</span></span>
<span data-ttu-id="fbc5f-114">Befejezési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="fbc5f-114">End Time in UTC</span></span>

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

### <span data-ttu-id="fbc5f-115">-Részletesség</span><span class="sxs-lookup"><span data-stu-id="fbc5f-115">-Granularity</span></span>
<span data-ttu-id="fbc5f-116">Granularitása</span><span class="sxs-lookup"><span data-stu-id="fbc5f-116">Granularity</span></span>

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

### <span data-ttu-id="fbc5f-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="fbc5f-117">-InstanceDetails</span></span>
<span data-ttu-id="fbc5f-118">Példány részletei</span><span class="sxs-lookup"><span data-stu-id="fbc5f-118">Instance Details</span></span>

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

### <span data-ttu-id="fbc5f-119">-Metrikák</span><span class="sxs-lookup"><span data-stu-id="fbc5f-119">-Metrics</span></span>
<span data-ttu-id="fbc5f-120">Metrikák karakterlánc-tömbként</span><span class="sxs-lookup"><span data-stu-id="fbc5f-120">Metrics as a string array</span></span>

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

### <span data-ttu-id="fbc5f-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fbc5f-121">-Name</span></span>
<span data-ttu-id="fbc5f-122">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="fbc5f-122">WebApp Name</span></span>

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

### <span data-ttu-id="fbc5f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc5f-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbc5f-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="fbc5f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="fbc5f-125">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="fbc5f-125">-StartTime</span></span>
<span data-ttu-id="fbc5f-126">Kezdési időpont az UTC-ban</span><span class="sxs-lookup"><span data-stu-id="fbc5f-126">Start Time in UTC</span></span>

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

### <span data-ttu-id="fbc5f-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fbc5f-127">-WebApp</span></span>
<span data-ttu-id="fbc5f-128">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="fbc5f-128">WebApp object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc5f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc5f-129">-DefaultProfile</span></span>
<span data-ttu-id="fbc5f-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbc5f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbc5f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc5f-131">CommonParameters</span></span>
<span data-ttu-id="fbc5f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbc5f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc5f-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbc5f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc5f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbc5f-134">INPUTS</span></span>

### <span data-ttu-id="fbc5f-135">Webhely</span><span class="sxs-lookup"><span data-stu-id="fbc5f-135">Site</span></span>
<span data-ttu-id="fbc5f-136">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="fbc5f-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fbc5f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbc5f-137">OUTPUTS</span></span>

## <span data-ttu-id="fbc5f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbc5f-138">NOTES</span></span>

## <span data-ttu-id="fbc5f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbc5f-139">RELATED LINKS</span></span>

[<span data-ttu-id="fbc5f-140">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="fbc5f-140">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

