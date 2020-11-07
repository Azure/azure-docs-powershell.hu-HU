---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 50384630658f7626ee02ca1dee223e82bf122ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680734"
---
# <span data-ttu-id="c0627-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c0627-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="c0627-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0627-102">SYNOPSIS</span></span>
<span data-ttu-id="c0627-103">Tároló fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c0627-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0627-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0627-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c0627-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0627-105">DESCRIPTION</span></span>
<span data-ttu-id="c0627-106">A **New-AzureRmStorageAccount** parancsmag egy Azure Storage-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c0627-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="c0627-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c0627-107">EXAMPLES</span></span>

### <span data-ttu-id="c0627-108">Példa 1: tárterület-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="c0627-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS"
```

<span data-ttu-id="c0627-109">Ez a parancs létrehoz egy tárolási fiókot az erőforráscsoport neve MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c0627-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="c0627-110">2. példa: a tárterület-titkosítást használó blob-tárolási fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="c0627-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="c0627-111">A parancs létrehoz egy blob-tároló fiókot, amely a forró hozzáférési típust használja.</span><span class="sxs-lookup"><span data-stu-id="c0627-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="c0627-112">A fiók engedélyezte a tárterület-titkosítást a blob-szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="c0627-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="c0627-113">3. példa: hozzon létre egy olyan tárolási fiókot, amely lehetővé teszi a tárterület-titkosítást a blob-és Fájlszolgáltatások számára, valamint létrehozhatja és hozzárendelheti az identitást az Azure-rendszerhez.</span><span class="sxs-lookup"><span data-stu-id="c0627-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="c0627-114">Ez a parancs létrehoz egy olyan tárolási fiókot, amely lehetővé tette a tárterület-titkosítást a blob és a Fájlszolgáltatások számára.</span><span class="sxs-lookup"><span data-stu-id="c0627-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="c0627-115">Egy identitást hoz létre, és hozzárendel egy olyan identitást, amellyel az Azure-kulccsal kezelheti a fiókok kulcsait.</span><span class="sxs-lookup"><span data-stu-id="c0627-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="c0627-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0627-116">PARAMETERS</span></span>

### <span data-ttu-id="c0627-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="c0627-117">-AccessTier</span></span>
<span data-ttu-id="c0627-118">A parancsmag által létrehozott tárolási fiók hozzáférési rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0627-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="c0627-119">A paraméter elfogadható értékei a következők: meleg és hűvös.</span><span class="sxs-lookup"><span data-stu-id="c0627-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="c0627-120">Ha a BlobStorage értékét adja meg a *Kind* paraméterhez, meg kell adnia a *AccessTier* paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="c0627-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="c0627-121">Ha *a tárterület* értékére vonatkozó értéket ad meg, ne adja meg a *AccessTier* paramétert.</span><span class="sxs-lookup"><span data-stu-id="c0627-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0627-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c0627-122">-AssignIdentity</span></span>
<span data-ttu-id="c0627-123">Új tárolási fiók identitásának létrehozása és hozzárendelése ehhez a tárterülethez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.</span><span class="sxs-lookup"><span data-stu-id="c0627-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c0627-124">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c0627-124">-CustomDomainName</span></span>
<span data-ttu-id="c0627-125">A tárolási fiók egyéni tartományának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0627-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="c0627-126">Az alapértelmezett érték a tárterület.</span><span class="sxs-lookup"><span data-stu-id="c0627-126">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0627-127">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="c0627-127">-EnableEncryptionService</span></span>
<span data-ttu-id="c0627-128">Azt jelzi, hogy ez a parancsmag engedélyezi-e a tárterület-titkosítási szolgáltatást a tárterületen.</span><span class="sxs-lookup"><span data-stu-id="c0627-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="c0627-129">Az Azure Blob és az Azure file Services támogatott.</span><span class="sxs-lookup"><span data-stu-id="c0627-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0627-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="c0627-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="c0627-131">Azt jelzi, hogy a tárolási fiók csak HTTPS-forgalmat engedélyez-e.</span><span class="sxs-lookup"><span data-stu-id="c0627-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

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

### <span data-ttu-id="c0627-132">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c0627-132">-InformationAction</span></span>
<span data-ttu-id="c0627-133">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="c0627-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c0627-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c0627-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c0627-135">Folytassa</span><span class="sxs-lookup"><span data-stu-id="c0627-135">Continue</span></span>
- <span data-ttu-id="c0627-136">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="c0627-136">Ignore</span></span>
- <span data-ttu-id="c0627-137">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="c0627-137">Inquire</span></span>
- <span data-ttu-id="c0627-138">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c0627-138">SilentlyContinue</span></span>
- <span data-ttu-id="c0627-139">állj</span><span class="sxs-lookup"><span data-stu-id="c0627-139">Stop</span></span>
- <span data-ttu-id="c0627-140">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="c0627-140">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0627-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c0627-141">-InformationVariable</span></span>
<span data-ttu-id="c0627-142">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="c0627-142">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0627-143">-Kind</span><span class="sxs-lookup"><span data-stu-id="c0627-143">-Kind</span></span>
<span data-ttu-id="c0627-144">A parancsmag által létrehozott tárolási fiók típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0627-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="c0627-145">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c0627-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c0627-146">Tárterület.</span><span class="sxs-lookup"><span data-stu-id="c0627-146">Storage.</span></span>
<span data-ttu-id="c0627-147">Általános célú tárolási fiók, amely támogatja a Blobs, a táblázatok, a várólisták, a fájlok és a lemezek tárolását.</span><span class="sxs-lookup"><span data-stu-id="c0627-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
 
- <span data-ttu-id="c0627-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="c0627-148">BlobStorage.</span></span>
<span data-ttu-id="c0627-149">BLOB-tároló fiók, amely támogatja a BLOB-tárolót.</span><span class="sxs-lookup"><span data-stu-id="c0627-149">Blob storage account which supports storage of Blobs only.</span></span>
 

<span data-ttu-id="c0627-150">Az alapértelmezett érték a tárterület.</span><span class="sxs-lookup"><span data-stu-id="c0627-150">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0627-151">-Hely</span><span class="sxs-lookup"><span data-stu-id="c0627-151">-Location</span></span>
<span data-ttu-id="c0627-152">A létrehozandó tárterület-fiók helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0627-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0627-153">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0627-153">-Name</span></span>
<span data-ttu-id="c0627-154">A létrehozandó tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0627-154">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="c0627-155">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c0627-155">-NetworkRuleSet</span></span>
<span data-ttu-id="c0627-156">Tárolási fiók NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c0627-156">Storage Account NetworkRuleSet</span></span>

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

### <span data-ttu-id="c0627-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0627-157">-ResourceGroupName</span></span>
<span data-ttu-id="c0627-158">Annak az erőforrás-csoportnak a nevét adja meg, amelybe a tárolási fiókot hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="c0627-158">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="c0627-159">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c0627-159">-SkuName</span></span>
<span data-ttu-id="c0627-160">Megadja annak a tárolási fióknak az SKU-nevét, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c0627-160">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="c0627-161">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c0627-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c0627-162">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="c0627-162">Standard_LRS.</span></span>
<span data-ttu-id="c0627-163">Helyileg redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="c0627-163">Locally-redundant storage.</span></span> 
- <span data-ttu-id="c0627-164">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="c0627-164">Standard_ZRS.</span></span>
<span data-ttu-id="c0627-165">Zóna – redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="c0627-165">Zone-redundant storage.</span></span>
- <span data-ttu-id="c0627-166">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="c0627-166">Standard_GRS.</span></span>
<span data-ttu-id="c0627-167">Geo-redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="c0627-167">Geo-redundant storage.</span></span> 
- <span data-ttu-id="c0627-168">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="c0627-168">Standard_RAGRS.</span></span>
<span data-ttu-id="c0627-169">Olvassa el az Access geo-redundáns tárterülete című témakört.</span><span class="sxs-lookup"><span data-stu-id="c0627-169">Read access geo-redundant storage.</span></span> 
- <span data-ttu-id="c0627-170">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="c0627-170">Premium_LRS.</span></span>
<span data-ttu-id="c0627-171">Prémium lokálisan redundáns tárterület.</span><span class="sxs-lookup"><span data-stu-id="c0627-171">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0627-172">-Címke</span><span class="sxs-lookup"><span data-stu-id="c0627-172">-Tag</span></span>
<span data-ttu-id="c0627-173">Ha a BlobStorage értékét adja meg a *Kind* paraméterhez, meg kell adnia a *AccessTier* paraméter értékét.</span><span class="sxs-lookup"><span data-stu-id="c0627-173">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="c0627-174">Ha *a tárterület* értékére vonatkozó értéket ad meg, ne adja meg a *AccessTier* paramétert.</span><span class="sxs-lookup"><span data-stu-id="c0627-174">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0627-175">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="c0627-175">-UseSubDomain</span></span>
<span data-ttu-id="c0627-176">Azt jelzi, hogy engedélyezi-e a közvetlen CName érvényesítést.</span><span class="sxs-lookup"><span data-stu-id="c0627-176">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0627-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0627-177">-DefaultProfile</span></span>
<span data-ttu-id="c0627-178">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0627-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0627-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0627-179">CommonParameters</span></span>
<span data-ttu-id="c0627-180">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0627-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0627-181">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0627-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0627-182">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0627-182">INPUTS</span></span>

## <span data-ttu-id="c0627-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0627-183">OUTPUTS</span></span>

## <span data-ttu-id="c0627-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0627-184">NOTES</span></span>

## <span data-ttu-id="c0627-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0627-185">RELATED LINKS</span></span>

[<span data-ttu-id="c0627-186">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c0627-186">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="c0627-187">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c0627-187">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="c0627-188">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c0627-188">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


