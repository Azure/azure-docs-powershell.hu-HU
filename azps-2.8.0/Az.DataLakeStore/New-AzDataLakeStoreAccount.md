---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 64af4b5d8bf159332c757982fcd1b2f7e949f3ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666827"
---
# <span data-ttu-id="ceb19-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ceb19-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="ceb19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ceb19-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb19-103">Új Data Lake Store-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="ceb19-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="ceb19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ceb19-104">SYNTAX</span></span>

### <span data-ttu-id="ceb19-105">UserOrSystemAssignedEncryption (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ceb19-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceb19-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="ceb19-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceb19-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ceb19-107">DESCRIPTION</span></span>
<span data-ttu-id="ceb19-108">A **New-AzDataLakeStoreAccount** parancsmag új Data Lake Store-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ceb19-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="ceb19-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ceb19-109">EXAMPLES</span></span>

### <span data-ttu-id="ceb19-110">1. példa: fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="ceb19-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="ceb19-111">Ez a parancs létrehoz egy ContosoADL nevű adattó-tároló fiókot a kelet-amerikai 2 helyhez.</span><span class="sxs-lookup"><span data-stu-id="ceb19-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="ceb19-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ceb19-112">PARAMETERS</span></span>

### <span data-ttu-id="ceb19-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="ceb19-113">-DefaultGroup</span></span>
<span data-ttu-id="ceb19-114">Annak a AzureActive a címtár-csoportnak az objektum-AZONOSÍTÓját adja meg, amely az új fájlok és mappák alapértelmezett csoportjának a tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="ceb19-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="ceb19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb19-115">-DefaultProfile</span></span>
<span data-ttu-id="ceb19-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ceb19-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ceb19-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="ceb19-117">-DisableEncryption</span></span>
<span data-ttu-id="ceb19-118">Azt jelzi, hogy a fiókhoz nem tartozik titkosítási titkosítási típus.</span><span class="sxs-lookup"><span data-stu-id="ceb19-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb19-119">-Titkosítás</span><span class="sxs-lookup"><span data-stu-id="ceb19-119">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb19-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="ceb19-120">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb19-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ceb19-121">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb19-122">-Verzió</span><span class="sxs-lookup"><span data-stu-id="ceb19-122">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb19-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="ceb19-123">-Location</span></span>
<span data-ttu-id="ceb19-124">A fiókhoz használni kívánt helyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="ceb19-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="ceb19-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ceb19-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ceb19-126">Kelet-amerikai 2</span><span class="sxs-lookup"><span data-stu-id="ceb19-126">East US 2</span></span>

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

### <span data-ttu-id="ceb19-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ceb19-127">-Name</span></span>
<span data-ttu-id="ceb19-128">A létrehozandó fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ceb19-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="ceb19-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceb19-129">-ResourceGroupName</span></span>
<span data-ttu-id="ceb19-130">A fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ceb19-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="ceb19-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="ceb19-131">-Tag</span></span>
<span data-ttu-id="ceb19-132">A címkéket kulcs-érték párokként adja meg.</span><span class="sxs-lookup"><span data-stu-id="ceb19-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="ceb19-133">Címkéket használhat a többi Azure-erőforrásból származó adattó-tároló fiók felismeréséhez.</span><span class="sxs-lookup"><span data-stu-id="ceb19-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="ceb19-134">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="ceb19-134">-Tier</span></span>
<span data-ttu-id="ceb19-135">A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="ceb19-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="ceb19-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb19-136">CommonParameters</span></span>
<span data-ttu-id="ceb19-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ceb19-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb19-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceb19-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb19-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceb19-139">INPUTS</span></span>

### <span data-ttu-id="ceb19-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ceb19-140">System.String</span></span>

### <span data-ttu-id="ceb19-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ceb19-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ceb19-142">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. EncryptionConfigType, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ceb19-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ceb19-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ceb19-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ceb19-144">System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. TierType, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ceb19-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ceb19-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceb19-145">OUTPUTS</span></span>

### <span data-ttu-id="ceb19-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ceb19-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="ceb19-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ceb19-147">NOTES</span></span>

## <span data-ttu-id="ceb19-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ceb19-148">RELATED LINKS</span></span>

[<span data-ttu-id="ceb19-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ceb19-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ceb19-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ceb19-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ceb19-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ceb19-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ceb19-152">Teszt-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ceb19-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


