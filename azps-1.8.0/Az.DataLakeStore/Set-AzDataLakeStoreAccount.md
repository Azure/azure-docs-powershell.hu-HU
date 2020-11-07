---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 0754bd515a846f8524bc7fd9826d36d19d79843a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836270"
---
# <span data-ttu-id="b3c6b-101">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b3c6b-101">Set-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="b3c6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c6b-103">Az adattó-tároló fiók módosítása.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-103">Modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="b3c6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3c6b-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3c6b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3c6b-105">DESCRIPTION</span></span>
<span data-ttu-id="b3c6b-106">A **set-AzDataLakeStoreAccount** parancsmag módosította az adattó-tároló fiókját.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-106">The **Set-AzDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="b3c6b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b3c6b-107">EXAMPLES</span></span>

### <span data-ttu-id="b3c6b-108">1. példa: címke hozzáadása egy fiókhoz</span><span class="sxs-lookup"><span data-stu-id="b3c6b-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="b3c6b-109">Ez a parancs hozzáadja a megadott címkét az ContosoADL nevű adattó-tároló fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="b3c6b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3c6b-110">PARAMETERS</span></span>

### <span data-ttu-id="b3c6b-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="b3c6b-111">-AllowAzureIpState</span></span>
<span data-ttu-id="b3c6b-112">Engedélyezze/tiltsa le az Azure-tól származó IP-ket a tűzfalon keresztül.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="b3c6b-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="b3c6b-113">-DefaultGroup</span></span>
<span data-ttu-id="b3c6b-114">Egy AzureActive-címtár-csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="b3c6b-115">Ez a csoport a létrehozott fájlok és mappák alapértelmezett csoportja.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-115">This group is the default group for files and folders that you create.</span></span>

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

### <span data-ttu-id="b3c6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c6b-116">-DefaultProfile</span></span>
<span data-ttu-id="b3c6b-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b3c6b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3c6b-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="b3c6b-118">-FirewallState</span></span>
<span data-ttu-id="b3c6b-119">Szükség esetén engedélyezze vagy tiltsa le a meglévő tűzfalszabályok szabályait.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-119">Optionally enable or disable existing firewall rules.</span></span>

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

### <span data-ttu-id="b3c6b-120">-Verzió</span><span class="sxs-lookup"><span data-stu-id="b3c6b-120">-KeyVersion</span></span>
<span data-ttu-id="b3c6b-121">Ha a titkosítási típus felhasználó által van hozzárendelve, a felhasználó elforgathatja a fontos verziót ezzel a paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

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

### <span data-ttu-id="b3c6b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b3c6b-122">-Name</span></span>
<span data-ttu-id="b3c6b-123">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="b3c6b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c6b-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3c6b-125">Annak a csoportnak a neve, amely a módosítani kívánt adattó-tároló fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="b3c6b-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="b3c6b-126">-Tag</span></span>
<span data-ttu-id="b3c6b-127">A címkéket kulcs-érték párokként adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="b3c6b-128">Címkéket használhat a többi Azure-erőforrásból származó adattó-tároló fiók felismeréséhez.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="b3c6b-129">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="b3c6b-129">-Tier</span></span>
<span data-ttu-id="b3c6b-130">A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="b3c6b-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="b3c6b-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="b3c6b-132">Szükség esetén engedélyezze vagy tiltsa le a meglévő megbízható azonosító-szolgáltatókat.</span><span class="sxs-lookup"><span data-stu-id="b3c6b-132">Optionally enable or disable the existing trusted ID providers.</span></span>

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

### <span data-ttu-id="b3c6b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c6b-133">CommonParameters</span></span>
<span data-ttu-id="b3c6b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3c6b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c6b-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3c6b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c6b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3c6b-136">INPUTS</span></span>

### <span data-ttu-id="b3c6b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b3c6b-137">System.String</span></span>

### <span data-ttu-id="b3c6b-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b3c6b-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b3c6b-139">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. TrustedIdProviderState, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b3c6b-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b3c6b-140">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. FirewallState, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b3c6b-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b3c6b-141">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. TierType, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b3c6b-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b3c6b-142">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b3c6b-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b3c6b-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3c6b-143">OUTPUTS</span></span>

### <span data-ttu-id="b3c6b-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b3c6b-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="b3c6b-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3c6b-145">NOTES</span></span>

## <span data-ttu-id="b3c6b-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3c6b-146">RELATED LINKS</span></span>

[<span data-ttu-id="b3c6b-147">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b3c6b-147">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b3c6b-148">Új – AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b3c6b-148">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b3c6b-149">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b3c6b-149">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b3c6b-150">Teszt-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b3c6b-150">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


