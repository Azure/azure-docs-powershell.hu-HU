---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 4bfbb25fa8b1e372175f741fd298384caa8050ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499612"
---
# <span data-ttu-id="e5bf6-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e5bf6-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="e5bf6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="e5bf6-103">Az adattó-típusú Analytics-fiók módosítása.</span><span class="sxs-lookup"><span data-stu-id="e5bf6-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5bf6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5bf6-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5bf6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5bf6-105">DESCRIPTION</span></span>
<span data-ttu-id="e5bf6-106">A **set-AzureRmDataLakeAnalyticsAccount** parancsmag az Azure Data Lake-tó Analytics-fiókját módosítja.</span><span class="sxs-lookup"><span data-stu-id="e5bf6-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e5bf6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e5bf6-107">EXAMPLES</span></span>

### <span data-ttu-id="e5bf6-108">Példa 1: a fiók adatforrásának módosítása</span><span class="sxs-lookup"><span data-stu-id="e5bf6-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="e5bf6-109">Ez a parancs megváltoztatja az alapértelmezett adatforrást és a címkék tulajdonságot a fiókban.</span><span class="sxs-lookup"><span data-stu-id="e5bf6-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="e5bf6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5bf6-110">PARAMETERS</span></span>

### <span data-ttu-id="e5bf6-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="e5bf6-111">-AllowAzureIpState</span></span>
<span data-ttu-id="e5bf6-112">Engedélyezze/tiltsa le az Azure-tól származó IP-ket a tűzfalon keresztül.</span><span class="sxs-lookup"><span data-stu-id="e5bf6-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5bf6-113">-DefaultProfile</span></span>
<span data-ttu-id="e5bf6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e5bf6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5bf6-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="e5bf6-115">-FirewallState</span></span>
<span data-ttu-id="e5bf6-116">Szükség esetén engedélyezze vagy tiltsa le a meglévő tűzfalszabályok szabályait.</span><span class="sxs-lookup"><span data-stu-id="e5bf6-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf6-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="e5bf6-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="e5bf6-118">A választható maximálisan támogatott elemzési egységek a fiók frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="e5bf6-118">The optional maximum supported analytics units to update the account with.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf6-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="e5bf6-119">-MaxJobCount</span></span>
<span data-ttu-id="e5bf6-120">A fiókban egyidejűleg futó, maximálisan támogatott feladatok száma a beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="e5bf6-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf6-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5bf6-121">-Name</span></span>
<span data-ttu-id="e5bf6-122">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5bf6-122">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf6-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="e5bf6-123">-QueryStoreRetention</span></span>
<span data-ttu-id="e5bf6-124">Azon napok tetszőleges száma, amelyekben a feladat metaadatai megmaradnak a fiókban való beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="e5bf6-124">The optional number of days that job metadata is retained to set in the account.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5bf6-125">-ResourceGroupName</span></span>
<span data-ttu-id="e5bf6-126">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5bf6-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf6-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="e5bf6-127">-Tag</span></span>
<span data-ttu-id="e5bf6-128">A fiókkal társított címkék karakterlánca, amely a jelenlegi címkék cseréjét adja vissza</span><span class="sxs-lookup"><span data-stu-id="e5bf6-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf6-129">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="e5bf6-129">-Tier</span></span>
<span data-ttu-id="e5bf6-130">A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="e5bf6-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bf6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5bf6-131">CommonParameters</span></span>
<span data-ttu-id="e5bf6-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5bf6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5bf6-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5bf6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5bf6-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5bf6-134">INPUTS</span></span>

### <span data-ttu-id="e5bf6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e5bf6-135">System.String</span></span>

### <span data-ttu-id="e5bf6-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e5bf6-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e5bf6-137">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e5bf6-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e5bf6-138">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. models. TierType, Microsoft. Azure. Management. DataLake. Analytics, Version = 3.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e5bf6-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e5bf6-139">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. models. FirewallState, Microsoft. Azure. Management. DataLake. Analytics, Version = 3.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e5bf6-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e5bf6-140">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. DataLake. Analytics, Version = 3.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e5bf6-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="e5bf6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5bf6-141">OUTPUTS</span></span>

### <span data-ttu-id="e5bf6-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e5bf6-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="e5bf6-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5bf6-143">NOTES</span></span>

## <span data-ttu-id="e5bf6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5bf6-144">RELATED LINKS</span></span>

[<span data-ttu-id="e5bf6-145">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e5bf6-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e5bf6-146">Új – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e5bf6-146">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e5bf6-147">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e5bf6-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e5bf6-148">Teszt-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e5bf6-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


