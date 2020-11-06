---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c9964bfb6d9f701d88a16b8a227aec7c2018a217
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493141"
---
# <span data-ttu-id="1e2bf-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1e2bf-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="1e2bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e2bf-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2bf-103">Új Data Lake Store-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="1e2bf-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e2bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e2bf-104">SYNTAX</span></span>

### <span data-ttu-id="1e2bf-105">UserOrSystemAssignedEncryption (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e2bf-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e2bf-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="1e2bf-106">DisableEncryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e2bf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e2bf-107">DESCRIPTION</span></span>
<span data-ttu-id="1e2bf-108">A **New-AzureRmDataLakeStoreAccount** parancsmag új Data Lake Store-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="1e2bf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1e2bf-109">EXAMPLES</span></span>

### <span data-ttu-id="1e2bf-110">1. példa: fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="1e2bf-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="1e2bf-111">Ez a parancs létrehoz egy ContosoADL nevű adattó-tároló fiókot a kelet-amerikai 2 helyhez.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="1e2bf-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e2bf-112">PARAMETERS</span></span>

### <span data-ttu-id="1e2bf-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="1e2bf-113">-DefaultGroup</span></span>
<span data-ttu-id="1e2bf-114">Annak a AzureActive a címtár-csoportnak az objektum-AZONOSÍTÓját adja meg, amely az új fájlok és mappák alapértelmezett csoportjának a tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="1e2bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e2bf-115">-DefaultProfile</span></span>
<span data-ttu-id="1e2bf-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1e2bf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e2bf-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="1e2bf-117">-DisableEncryption</span></span>
<span data-ttu-id="1e2bf-118">Azt jelzi, hogy a fiókhoz nem tartozik titkosítási titkosítási típus.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2bf-119">-Titkosítás</span><span class="sxs-lookup"><span data-stu-id="1e2bf-119">-Encryption</span></span>
```yaml
Type: EncryptionConfigType
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2bf-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="1e2bf-120">-KeyName</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2bf-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1e2bf-121">-KeyVaultId</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2bf-122">-Verzió</span><span class="sxs-lookup"><span data-stu-id="1e2bf-122">-KeyVersion</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2bf-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="1e2bf-123">-Location</span></span>
<span data-ttu-id="1e2bf-124">A fiókhoz használni kívánt helyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="1e2bf-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1e2bf-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e2bf-126">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="1e2bf-126">East US 2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2bf-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e2bf-127">-Name</span></span>
<span data-ttu-id="1e2bf-128">A létrehozandó fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-128">Specifies the name of the account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2bf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e2bf-129">-ResourceGroupName</span></span>
<span data-ttu-id="1e2bf-130">A fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="1e2bf-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="1e2bf-131">-Tag</span></span>
<span data-ttu-id="1e2bf-132">A címkéket kulcs-érték párokként adja meg.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="1e2bf-133">Címkéket használhat a többi Azure-erőforrásból származó adattó-tároló fiók felismeréséhez.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e2bf-134">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="1e2bf-134">-Tier</span></span>
<span data-ttu-id="1e2bf-135">A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="1e2bf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2bf-136">CommonParameters</span></span>
<span data-ttu-id="1e2bf-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e2bf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2bf-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e2bf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2bf-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e2bf-139">INPUTS</span></span>

### <span data-ttu-id="1e2bf-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="1e2bf-140">None</span></span>
<span data-ttu-id="1e2bf-141">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e2bf-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e2bf-142">OUTPUTS</span></span>

### <span data-ttu-id="1e2bf-143">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1e2bf-143">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="1e2bf-144">A létrehozott fiók adatai.</span><span class="sxs-lookup"><span data-stu-id="1e2bf-144">The created account details.</span></span>

## <span data-ttu-id="1e2bf-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e2bf-145">NOTES</span></span>

## <span data-ttu-id="1e2bf-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e2bf-146">RELATED LINKS</span></span>

[<span data-ttu-id="1e2bf-147">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1e2bf-147">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="1e2bf-148">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1e2bf-148">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="1e2bf-149">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1e2bf-149">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="1e2bf-150">Teszt-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="1e2bf-150">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


