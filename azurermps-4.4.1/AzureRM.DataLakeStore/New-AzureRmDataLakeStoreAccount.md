---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b05cb9e3789afa905da93642929f65f4965f9b0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680893"
---
# <span data-ttu-id="290d8-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="290d8-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="290d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="290d8-102">SYNOPSIS</span></span>
<span data-ttu-id="290d8-103">Új Data Lake Store-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="290d8-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="290d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="290d8-104">SYNTAX</span></span>

### <span data-ttu-id="290d8-105">Felhasználó vagy rendszerhez rendelt titkosítás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="290d8-105">User or System assigned encryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="290d8-106">Titkosítás letiltása</span><span class="sxs-lookup"><span data-stu-id="290d8-106">Disable Encryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="290d8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="290d8-107">DESCRIPTION</span></span>
<span data-ttu-id="290d8-108">A **New-AzureRmDataLakeStoreAccount** parancsmag új Data Lake Store-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="290d8-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="290d8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="290d8-109">EXAMPLES</span></span>

### <span data-ttu-id="290d8-110">1. példa: fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="290d8-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="290d8-111">Ez a parancs létrehoz egy ContosoADL nevű adattó-tároló fiókot a kelet-amerikai 2 helyhez.</span><span class="sxs-lookup"><span data-stu-id="290d8-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="290d8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="290d8-112">PARAMETERS</span></span>

### <span data-ttu-id="290d8-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="290d8-113">-DefaultGroup</span></span>
<span data-ttu-id="290d8-114">Annak a AzureActive a címtár-csoportnak az objektum-AZONOSÍTÓját adja meg, amely az új fájlok és mappák alapértelmezett csoportjának a tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="290d8-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="290d8-115">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="290d8-115">-DisableEncryption</span></span>
<span data-ttu-id="290d8-116">Azt jelzi, hogy a fiókhoz nem tartozik titkosítási titkosítási típus.</span><span class="sxs-lookup"><span data-stu-id="290d8-116">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Encryption
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="290d8-117">-Titkosítás</span><span class="sxs-lookup"><span data-stu-id="290d8-117">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: User or System assigned encryption
Aliases: 
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="290d8-118">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="290d8-118">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="290d8-119">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="290d8-119">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="290d8-120">-Verzió</span><span class="sxs-lookup"><span data-stu-id="290d8-120">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="290d8-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="290d8-121">-Location</span></span>
<span data-ttu-id="290d8-122">A fiókhoz használni kívánt helyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="290d8-122">Specifies the location to use for the account.</span></span>
<span data-ttu-id="290d8-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="290d8-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="290d8-124">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="290d8-124">East US 2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="290d8-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="290d8-125">-Name</span></span>
<span data-ttu-id="290d8-126">A létrehozandó fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="290d8-126">Specifies the name of the account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="290d8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="290d8-127">-ResourceGroupName</span></span>
<span data-ttu-id="290d8-128">A fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="290d8-128">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="290d8-129">-Címkék</span><span class="sxs-lookup"><span data-stu-id="290d8-129">-Tags</span></span>
<span data-ttu-id="290d8-130">A címkéket kulcs-érték párokként adja meg.</span><span class="sxs-lookup"><span data-stu-id="290d8-130">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="290d8-131">Címkéket használhat a többi Azure-erőforrásból származó adattó-tároló fiók felismeréséhez.</span><span class="sxs-lookup"><span data-stu-id="290d8-131">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="290d8-132">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="290d8-132">-Tier</span></span>
<span data-ttu-id="290d8-133">A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="290d8-133">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="290d8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="290d8-134">-DefaultProfile</span></span>
<span data-ttu-id="290d8-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="290d8-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="290d8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="290d8-136">CommonParameters</span></span>
<span data-ttu-id="290d8-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="290d8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="290d8-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="290d8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="290d8-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="290d8-139">INPUTS</span></span>

## <span data-ttu-id="290d8-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="290d8-140">OUTPUTS</span></span>

### <span data-ttu-id="290d8-141">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="290d8-141">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="290d8-142">A létrehozott fiók adatai.</span><span class="sxs-lookup"><span data-stu-id="290d8-142">The created account details.</span></span>

## <span data-ttu-id="290d8-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="290d8-143">NOTES</span></span>

## <span data-ttu-id="290d8-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="290d8-144">RELATED LINKS</span></span>

[<span data-ttu-id="290d8-145">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="290d8-145">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="290d8-146">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="290d8-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="290d8-147">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="290d8-147">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="290d8-148">Teszt-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="290d8-148">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


