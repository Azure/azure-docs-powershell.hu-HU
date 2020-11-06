---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8de6b2a0d86c9eb83a067f4982a5ef62d3a9adbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493539"
---
# <span data-ttu-id="44906-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="44906-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="44906-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44906-102">SYNOPSIS</span></span>
<span data-ttu-id="44906-103">Az adattó-típusú Analytics-fiók módosítása.</span><span class="sxs-lookup"><span data-stu-id="44906-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44906-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44906-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tags] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxDegreeOfParallelism <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44906-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="44906-105">DESCRIPTION</span></span>
<span data-ttu-id="44906-106">A **set-AzureRmDataLakeAnalyticsAccount** parancsmag az Azure Data Lake-tó Analytics-fiókját módosítja.</span><span class="sxs-lookup"><span data-stu-id="44906-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="44906-107">Példák</span><span class="sxs-lookup"><span data-stu-id="44906-107">EXAMPLES</span></span>

### <span data-ttu-id="44906-108">Példa 1: a fiók adatforrásának módosítása</span><span class="sxs-lookup"><span data-stu-id="44906-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="44906-109">Ez a parancs megváltoztatja az alapértelmezett adatforrást és a címkék tulajdonságot a fiókban.</span><span class="sxs-lookup"><span data-stu-id="44906-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="44906-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44906-110">PARAMETERS</span></span>

### <span data-ttu-id="44906-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="44906-111">-AllowAzureIpState</span></span>
<span data-ttu-id="44906-112">Engedélyezze/tiltsa le az Azure-tól származó IP-ket a tűzfalon keresztül.</span><span class="sxs-lookup"><span data-stu-id="44906-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="44906-113">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="44906-113">-FirewallState</span></span>
<span data-ttu-id="44906-114">Szükség esetén engedélyezze vagy tiltsa le a meglévő tűzfalszabályok szabályait.</span><span class="sxs-lookup"><span data-stu-id="44906-114">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="44906-115">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="44906-115">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="44906-116">A nem kötelező maximálisan támogatott párhuzamossági mérték a fiók frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="44906-116">The optional maximum supported degree of parallelism to update the account with.</span></span>

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

### <span data-ttu-id="44906-117">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="44906-117">-MaxJobCount</span></span>
<span data-ttu-id="44906-118">A fiókban egyidejűleg futó, maximálisan támogatott feladatok száma a beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="44906-118">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="44906-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="44906-119">-Name</span></span>
<span data-ttu-id="44906-120">A Lake Analytics-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="44906-120">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="44906-121">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="44906-121">-QueryStoreRetention</span></span>
<span data-ttu-id="44906-122">Azon napok tetszőleges száma, amelyekben a feladat metaadatai megmaradnak a fiókban való beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="44906-122">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="44906-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44906-123">-ResourceGroupName</span></span>
<span data-ttu-id="44906-124">Az adattó-adatkezelési fiók erőforráscsoport-nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="44906-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="44906-125">-Címkék</span><span class="sxs-lookup"><span data-stu-id="44906-125">-Tags</span></span>
<span data-ttu-id="44906-126">Azokat a kulcs-érték párokat adja meg, amelyek a többi Azure-erőforrás között a Data Lake Analytics-fiók felismerésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="44906-126">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

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

### <span data-ttu-id="44906-127">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="44906-127">-Tier</span></span>
<span data-ttu-id="44906-128">A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="44906-128">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="44906-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44906-129">-DefaultProfile</span></span>
<span data-ttu-id="44906-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44906-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44906-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44906-131">CommonParameters</span></span>
<span data-ttu-id="44906-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44906-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44906-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44906-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44906-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44906-134">INPUTS</span></span>

## <span data-ttu-id="44906-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44906-135">OUTPUTS</span></span>

### <span data-ttu-id="44906-136">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="44906-136">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="44906-137">A fiókadatok frissített ismertetése.</span><span class="sxs-lookup"><span data-stu-id="44906-137">The updated account details.</span></span>

## <span data-ttu-id="44906-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44906-138">NOTES</span></span>

## <span data-ttu-id="44906-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44906-139">RELATED LINKS</span></span>

[<span data-ttu-id="44906-140">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="44906-140">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="44906-141">Új – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="44906-141">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="44906-142">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="44906-142">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="44906-143">Teszt-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="44906-143">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


