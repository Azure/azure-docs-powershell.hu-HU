---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4db6ceb0f806aeffd4dc69580da891de567e4e83
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94015036"
---
# <span data-ttu-id="e6fb0-101">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e6fb0-101">Set-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="e6fb0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="e6fb0-103">Az adattó-tároló fiók módosítása.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-103">Modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="e6fb0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6fb0-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6fb0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6fb0-105">DESCRIPTION</span></span>
<span data-ttu-id="e6fb0-106">A **set-AzDataLakeStoreAccount** parancsmag módosította az adattó-tároló fiókját.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-106">The **Set-AzDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="e6fb0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e6fb0-107">EXAMPLES</span></span>

### <span data-ttu-id="e6fb0-108">1. példa: címke hozzáadása egy fiókhoz</span><span class="sxs-lookup"><span data-stu-id="e6fb0-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="e6fb0-109">Ez a parancs hozzáadja a megadott címkét az ContosoADL nevű adattó-tároló fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="e6fb0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6fb0-110">PARAMETERS</span></span>

### <span data-ttu-id="e6fb0-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="e6fb0-111">-AllowAzureIpState</span></span>
<span data-ttu-id="e6fb0-112">Engedélyezze/tiltsa le az Azure-tól származó IP-ket a tűzfalon keresztül.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fb0-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="e6fb0-113">-DefaultGroup</span></span>
<span data-ttu-id="e6fb0-114">Egy AzureActive-címtár-csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="e6fb0-115">Ez a csoport a létrehozott fájlok és mappák alapértelmezett csoportja.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6fb0-116">-DefaultProfile</span></span>
<span data-ttu-id="e6fb0-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e6fb0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6fb0-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="e6fb0-118">-FirewallState</span></span>
<span data-ttu-id="e6fb0-119">Szükség esetén engedélyezze vagy tiltsa le a meglévő tűzfalszabályok szabályait.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fb0-120">-Verzió</span><span class="sxs-lookup"><span data-stu-id="e6fb0-120">-KeyVersion</span></span>
<span data-ttu-id="e6fb0-121">Ha a titkosítási típus felhasználó által van hozzárendelve, a felhasználó elforgathatja a fontos verziót ezzel a paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fb0-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6fb0-122">-Name</span></span>
<span data-ttu-id="e6fb0-123">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="e6fb0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6fb0-124">-ResourceGroupName</span></span>
<span data-ttu-id="e6fb0-125">Annak a csoportnak a neve, amely a módosítani kívánt adattó-tároló fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fb0-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="e6fb0-126">-Tag</span></span>
<span data-ttu-id="e6fb0-127">A címkéket kulcs-érték párokként adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="e6fb0-128">Címkéket használhat a többi Azure-erőforrásból származó adattó-tároló fiók felismeréséhez.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fb0-129">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="e6fb0-129">-Tier</span></span>
<span data-ttu-id="e6fb0-130">A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fb0-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="e6fb0-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="e6fb0-132">Szükség esetén engedélyezze vagy tiltsa le a meglévő megbízható azonosító-szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="e6fb0-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fb0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6fb0-133">CommonParameters</span></span>
<span data-ttu-id="e6fb0-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6fb0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6fb0-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6fb0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6fb0-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6fb0-136">INPUTS</span></span>

### <span data-ttu-id="e6fb0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e6fb0-137">System.String</span></span>

### <span data-ttu-id="e6fb0-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6fb0-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e6fb0-139">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. TrustedIdProviderState, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e6fb0-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e6fb0-140">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. FirewallState, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e6fb0-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e6fb0-141">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. TierType, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e6fb0-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e6fb0-142">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e6fb0-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="e6fb0-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6fb0-143">OUTPUTS</span></span>

### <span data-ttu-id="e6fb0-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e6fb0-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="e6fb0-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6fb0-145">NOTES</span></span>

## <span data-ttu-id="e6fb0-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6fb0-146">RELATED LINKS</span></span>

[<span data-ttu-id="e6fb0-147">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e6fb0-147">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e6fb0-148">Új – AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e6fb0-148">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e6fb0-149">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e6fb0-149">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e6fb0-150">Teszt-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e6fb0-150">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


