---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 22eac04b24e8fec1778578f4e54792b5dcde6d1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504576"
---
# <span data-ttu-id="e2119-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e2119-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="e2119-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2119-102">SYNOPSIS</span></span>
<span data-ttu-id="e2119-103">Az adattó-tároló fiók módosítása.</span><span class="sxs-lookup"><span data-stu-id="e2119-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2119-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2119-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2119-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2119-105">DESCRIPTION</span></span>
<span data-ttu-id="e2119-106">A **set-AzureRmDataLakeStoreAccount** parancsmag módosította az adattó-tároló fiókját.</span><span class="sxs-lookup"><span data-stu-id="e2119-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="e2119-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e2119-107">EXAMPLES</span></span>

### <span data-ttu-id="e2119-108">1. példa: címke hozzáadása egy fiókhoz</span><span class="sxs-lookup"><span data-stu-id="e2119-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="e2119-109">Ez a parancs hozzáadja a megadott címkét az ContosoADL nevű adattó-tároló fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="e2119-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="e2119-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2119-110">PARAMETERS</span></span>

### <span data-ttu-id="e2119-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="e2119-111">-AllowAzureIpState</span></span>
<span data-ttu-id="e2119-112">Engedélyezze/tiltsa le az Azure-tól származó IP-ket a tűzfalon keresztül.</span><span class="sxs-lookup"><span data-stu-id="e2119-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2119-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="e2119-113">-DefaultGroup</span></span>
<span data-ttu-id="e2119-114">Egy AzureActive-címtár-csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2119-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="e2119-115">Ez a csoport a létrehozott fájlok és mappák alapértelmezett csoportja.</span><span class="sxs-lookup"><span data-stu-id="e2119-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2119-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2119-116">-DefaultProfile</span></span>
<span data-ttu-id="e2119-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e2119-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2119-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="e2119-118">-FirewallState</span></span>
<span data-ttu-id="e2119-119">Szükség esetén engedélyezze vagy tiltsa le a meglévő tűzfalszabályok szabályait.</span><span class="sxs-lookup"><span data-stu-id="e2119-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2119-120">-Verzió</span><span class="sxs-lookup"><span data-stu-id="e2119-120">-KeyVersion</span></span>
<span data-ttu-id="e2119-121">Ha a titkosítási típus felhasználó által van hozzárendelve, a felhasználó elforgathatja a fontos verziót ezzel a paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="e2119-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2119-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2119-122">-Name</span></span>
<span data-ttu-id="e2119-123">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2119-123">Specifies the name of a Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2119-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2119-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2119-125">Annak a csoportnak a neve, amely a módosítani kívánt adattó-tároló fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e2119-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2119-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="e2119-126">-Tag</span></span>
<span data-ttu-id="e2119-127">A címkéket kulcs-érték párokként adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2119-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="e2119-128">Címkéket használhat a többi Azure-erőforrásból származó adattó-tároló fiók felismeréséhez.</span><span class="sxs-lookup"><span data-stu-id="e2119-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2119-129">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="e2119-129">-Tier</span></span>
<span data-ttu-id="e2119-130">A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="e2119-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2119-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="e2119-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="e2119-132">Szükség esetén engedélyezze vagy tiltsa le a meglévő megbízható azonosító-szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="e2119-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: TrustedIdProviderState
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2119-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2119-133">CommonParameters</span></span>
<span data-ttu-id="e2119-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2119-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2119-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2119-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2119-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2119-136">INPUTS</span></span>

### <span data-ttu-id="e2119-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="e2119-137">None</span></span>
<span data-ttu-id="e2119-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e2119-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2119-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2119-139">OUTPUTS</span></span>

### <span data-ttu-id="e2119-140">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e2119-140">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="e2119-141">A fiókadatok frissített ismertetése.</span><span class="sxs-lookup"><span data-stu-id="e2119-141">The updated account details.</span></span>

## <span data-ttu-id="e2119-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2119-142">NOTES</span></span>

## <span data-ttu-id="e2119-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2119-143">RELATED LINKS</span></span>

[<span data-ttu-id="e2119-144">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e2119-144">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="e2119-145">Új – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e2119-145">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="e2119-146">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e2119-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="e2119-147">Teszt-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e2119-147">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


