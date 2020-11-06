---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 2ceb395805607809593054880415dccac7e1e28c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498160"
---
# <span data-ttu-id="e28f6-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e28f6-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="e28f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e28f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e28f6-103">Tároló fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e28f6-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e28f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e28f6-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>]
 [-UseSubDomain <Boolean>] [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e28f6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e28f6-105">DESCRIPTION</span></span>
<span data-ttu-id="e28f6-106">A **New-AzureRmStorageAccount** parancsmag egy Azure Storage-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e28f6-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="e28f6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e28f6-107">EXAMPLES</span></span>

### <span data-ttu-id="e28f6-108">Példa 1: tárterület-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="e28f6-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="e28f6-109">Ez a parancs létrehoz egy tárolási fiókot az erőforráscsoport neve MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e28f6-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="e28f6-110">2. példa: blob-tároló létrehozása a BlobStorage-féle és a forró AccessTier</span><span class="sxs-lookup"><span data-stu-id="e28f6-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="e28f6-111">Ez a parancs olyan blob-tárterületet hoz létre, amely BlobStorage típusú és forró AccessTier</span><span class="sxs-lookup"><span data-stu-id="e28f6-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="e28f6-112">3. példa: hozzon létre egy Kind StorageV2 tároló fiókot, és hozzon létre és rendeljen identitást az Azure.</span><span class="sxs-lookup"><span data-stu-id="e28f6-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="e28f6-113">Ez a parancs a Kind StorageV2 létrehoz egy tárterület-fiókot.</span><span class="sxs-lookup"><span data-stu-id="e28f6-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="e28f6-114">Egy identitást hoz létre, és hozzárendel egy olyan identitást, amellyel az Azure-kulccsal kezelheti a fiókok kulcsait.</span><span class="sxs-lookup"><span data-stu-id="e28f6-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="e28f6-115">Példa 4: a NetworkRuleSet származó tárhely-fiók létrehozása a JSON-ról</span><span class="sxs-lookup"><span data-stu-id="e28f6-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="e28f6-116">Ez a parancs létrehoz egy olyan tárolási fiókot, amely a NetworkRuleSet tulajdonságot tartalmazza a JSON-ról</span><span class="sxs-lookup"><span data-stu-id="e28f6-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

## <span data-ttu-id="e28f6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e28f6-117">PARAMETERS</span></span>

### <span data-ttu-id="e28f6-118">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="e28f6-118">-AccessTier</span></span>
<span data-ttu-id="e28f6-119">A parancsmag által létrehozott tárolási fiók hozzáférési rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e28f6-119">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="e28f6-120">A paraméter elfogadható értékei a következők: meleg és hűvös.</span><span class="sxs-lookup"><span data-stu-id="e28f6-120">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="e28f6-121">Ha a BlobStorage értékét adja meg a *Kind* paraméterhez, meg kell adnia a *AccessTier* paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="e28f6-121">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="e28f6-122">Ha *a tárterület* értékére vonatkozó értéket ad meg, ne adja meg a *AccessTier* paramétert.</span><span class="sxs-lookup"><span data-stu-id="e28f6-122">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e28f6-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e28f6-123">-AsJob</span></span>
<span data-ttu-id="e28f6-124">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e28f6-124">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e28f6-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e28f6-125">-AssignIdentity</span></span>
<span data-ttu-id="e28f6-126">Új tárolási fiók identitásának létrehozása és hozzárendelése ehhez a tárterülethez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="e28f6-126">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e28f6-127">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="e28f6-127">-CustomDomainName</span></span>
<span data-ttu-id="e28f6-128">A tárolási fiók egyéni tartományának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e28f6-128">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="e28f6-129">Az alapértelmezett érték a tárterület.</span><span class="sxs-lookup"><span data-stu-id="e28f6-129">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e28f6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e28f6-130">-DefaultProfile</span></span>
<span data-ttu-id="e28f6-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e28f6-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e28f6-132">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="e28f6-132">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="e28f6-133">Azt jelzi, hogy a tárolási fiók csak HTTPS-forgalmat engedélyez-e.</span><span class="sxs-lookup"><span data-stu-id="e28f6-133">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28f6-134">-Kind</span><span class="sxs-lookup"><span data-stu-id="e28f6-134">-Kind</span></span>
<span data-ttu-id="e28f6-135">A parancsmag által létrehozott tárolási fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e28f6-135">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="e28f6-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e28f6-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e28f6-137">Tárterület.</span><span class="sxs-lookup"><span data-stu-id="e28f6-137">Storage.</span></span> <span data-ttu-id="e28f6-138">Általános célú tárolási fiók, amely támogatja a Blobs, a táblázatok, a várólisták, a fájlok és a lemezek tárolását.</span><span class="sxs-lookup"><span data-stu-id="e28f6-138">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="e28f6-139">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="e28f6-139">StorageV2.</span></span> <span data-ttu-id="e28f6-140">Általános célú 2-es verzió (GPv2) tárterülete, melyen a festékfoltok, a táblázatok, a várólisták, a fájlok és a lemezek a speciális funkciók, például az adatrétegek támogatása.</span><span class="sxs-lookup"><span data-stu-id="e28f6-140">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="e28f6-141">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="e28f6-141">BlobStorage.</span></span> <span data-ttu-id="e28f6-142">BLOB-tároló fiók, amely támogatja a BLOB-tárolót.</span><span class="sxs-lookup"><span data-stu-id="e28f6-142">Blob Storage account which supports storage of Blobs only.</span></span>
<span data-ttu-id="e28f6-143">Az alapértelmezett érték a tárterület.</span><span class="sxs-lookup"><span data-stu-id="e28f6-143">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e28f6-144">-Hely</span><span class="sxs-lookup"><span data-stu-id="e28f6-144">-Location</span></span>
<span data-ttu-id="e28f6-145">A létrehozandó tárterület-fiók helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e28f6-145">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28f6-146">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e28f6-146">-Name</span></span>
<span data-ttu-id="e28f6-147">A létrehozandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e28f6-147">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28f6-148">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e28f6-148">-NetworkRuleSet</span></span>
<span data-ttu-id="e28f6-149">A NetworkRuleSet a tűzfalakra és a virtuális hálózatokra vonatkozó konfigurációs szabályok halmazát, valamint a hálózati tulajdonságok, például a szabályok megkerülését lehetővé tevő, valamint a meghatározott szabályoknak nem megfelelő kérelmek kezelésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="e28f6-149">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e28f6-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e28f6-150">-ResourceGroupName</span></span>
<span data-ttu-id="e28f6-151">Annak az erőforrás-csoportnak a nevét adja meg, amelybe a tárolási fiókot hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="e28f6-151">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="e28f6-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e28f6-152">-SkuName</span></span>
<span data-ttu-id="e28f6-153">Megadja annak a tárolási fióknak az SKU-nevét, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e28f6-153">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="e28f6-154">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e28f6-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e28f6-155">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="e28f6-155">Standard_LRS.</span></span> <span data-ttu-id="e28f6-156">Helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="e28f6-156">Locally-redundant storage.</span></span>
- <span data-ttu-id="e28f6-157">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="e28f6-157">Standard_ZRS.</span></span> <span data-ttu-id="e28f6-158">Zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="e28f6-158">Zone-redundant storage.</span></span>
- <span data-ttu-id="e28f6-159">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="e28f6-159">Standard_GRS.</span></span> <span data-ttu-id="e28f6-160">Geo-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="e28f6-160">Geo-redundant storage.</span></span>
- <span data-ttu-id="e28f6-161">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="e28f6-161">Standard_RAGRS.</span></span> <span data-ttu-id="e28f6-162">Olvassa el az Access geo-redundáns tárterülete című témakört.</span><span class="sxs-lookup"><span data-stu-id="e28f6-162">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="e28f6-163">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="e28f6-163">Premium_LRS.</span></span> <span data-ttu-id="e28f6-164">Prémium lokálisan redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="e28f6-164">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28f6-165">-Címke</span><span class="sxs-lookup"><span data-stu-id="e28f6-165">-Tag</span></span>
<span data-ttu-id="e28f6-166">A kulcs-érték párok a kiszolgálón címkékként beállított kivonatoló táblázat formájában.</span><span class="sxs-lookup"><span data-stu-id="e28f6-166">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="e28f6-167">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="e28f6-167">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e28f6-168">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="e28f6-168">-UseSubDomain</span></span>
<span data-ttu-id="e28f6-169">Azt jelzi, hogy engedélyezi-e a közvetlen CName érvényesítést.</span><span class="sxs-lookup"><span data-stu-id="e28f6-169">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e28f6-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e28f6-170">CommonParameters</span></span>
<span data-ttu-id="e28f6-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e28f6-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e28f6-172">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e28f6-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e28f6-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e28f6-173">INPUTS</span></span>

### <span data-ttu-id="e28f6-174">System. String</span><span class="sxs-lookup"><span data-stu-id="e28f6-174">System.String</span></span>

### <span data-ttu-id="e28f6-175">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e28f6-175">System.Boolean</span></span>

## <span data-ttu-id="e28f6-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e28f6-176">OUTPUTS</span></span>

### <span data-ttu-id="e28f6-177">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e28f6-177">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e28f6-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e28f6-178">NOTES</span></span>

## <span data-ttu-id="e28f6-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e28f6-179">RELATED LINKS</span></span>

[<span data-ttu-id="e28f6-180">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e28f6-180">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="e28f6-181">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e28f6-181">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="e28f6-182">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e28f6-182">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
