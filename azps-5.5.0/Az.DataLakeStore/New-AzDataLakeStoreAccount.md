---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4bdf13b485486a8e3c40023ea0011d12b21a93b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204351"
---
# <span data-ttu-id="d69f8-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d69f8-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="d69f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d69f8-102">SYNOPSIS</span></span>
<span data-ttu-id="d69f8-103">Új Data Lake Store-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d69f8-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="d69f8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d69f8-104">SYNTAX</span></span>

### <span data-ttu-id="d69f8-105">UserOrSystemAssignedEncryption (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d69f8-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d69f8-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="d69f8-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d69f8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d69f8-107">DESCRIPTION</span></span>
<span data-ttu-id="d69f8-108">A **New-AzDataLakeStoreAccount** parancsmag létrehoz egy új Data Lake Store-fiókot.</span><span class="sxs-lookup"><span data-stu-id="d69f8-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="d69f8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d69f8-109">EXAMPLES</span></span>

### <span data-ttu-id="d69f8-110">1. példa: Fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="d69f8-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="d69f8-111">Ez a parancs létrehoz egy ContosoADL nevű Data Lake Store-fiókot az Egyesült Államok 2. keleti helyére.</span><span class="sxs-lookup"><span data-stu-id="d69f8-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="d69f8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d69f8-112">PARAMETERS</span></span>

### <span data-ttu-id="d69f8-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="d69f8-113">-DefaultGroup</span></span>
<span data-ttu-id="d69f8-114">Megadja annak az AzureActive Directory-csoportnak az objektumazonosítóját, amely az új fájlok és mappák alapértelmezett csoporttulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="d69f8-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="d69f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69f8-115">-DefaultProfile</span></span>
<span data-ttu-id="d69f8-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d69f8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d69f8-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="d69f8-117">-DisableEncryption</span></span>
<span data-ttu-id="d69f8-118">Azt jelzi, hogy a fiókra semmilyen titkosítási formában nem lesz alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="d69f8-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

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

### <span data-ttu-id="d69f8-119">-Encryption</span><span class="sxs-lookup"><span data-stu-id="d69f8-119">-Encryption</span></span>
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

### <span data-ttu-id="d69f8-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d69f8-120">-KeyName</span></span>
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

### <span data-ttu-id="d69f8-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="d69f8-121">-KeyVaultId</span></span>
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

### <span data-ttu-id="d69f8-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="d69f8-122">-KeyVersion</span></span>
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

### <span data-ttu-id="d69f8-123">-Location</span><span class="sxs-lookup"><span data-stu-id="d69f8-123">-Location</span></span>
<span data-ttu-id="d69f8-124">A fiókhoz használni használt hely.</span><span class="sxs-lookup"><span data-stu-id="d69f8-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="d69f8-125">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="d69f8-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d69f8-126">Us 2. kelet</span><span class="sxs-lookup"><span data-stu-id="d69f8-126">East US 2</span></span>

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

### <span data-ttu-id="d69f8-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d69f8-127">-Name</span></span>
<span data-ttu-id="d69f8-128">A létrehozni szükséges fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d69f8-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="d69f8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d69f8-129">-ResourceGroupName</span></span>
<span data-ttu-id="d69f8-130">A fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d69f8-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="d69f8-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="d69f8-131">-Tag</span></span>
<span data-ttu-id="d69f8-132">Kulcsérték-párokként adja meg a címkéket.</span><span class="sxs-lookup"><span data-stu-id="d69f8-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="d69f8-133">Címkékkel azonosíthatja a Data Lake Store-fiókokat más Azure-erőforrásokból.</span><span class="sxs-lookup"><span data-stu-id="d69f8-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="d69f8-134">-Tier</span><span class="sxs-lookup"><span data-stu-id="d69f8-134">-Tier</span></span>
<span data-ttu-id="d69f8-135">A fiókhoz használni kívánt kötelezettségvállalási szint.</span><span class="sxs-lookup"><span data-stu-id="d69f8-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="d69f8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69f8-136">CommonParameters</span></span>
<span data-ttu-id="d69f8-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d69f8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69f8-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d69f8-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69f8-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d69f8-139">INPUTS</span></span>

### <span data-ttu-id="d69f8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d69f8-140">System.String</span></span>

### <span data-ttu-id="d69f8-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d69f8-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d69f8-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d69f8-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d69f8-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d69f8-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d69f8-144">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d69f8-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d69f8-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d69f8-145">OUTPUTS</span></span>

### <span data-ttu-id="d69f8-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d69f8-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="d69f8-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d69f8-147">NOTES</span></span>

## <span data-ttu-id="d69f8-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d69f8-148">RELATED LINKS</span></span>

[<span data-ttu-id="d69f8-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d69f8-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="d69f8-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d69f8-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="d69f8-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d69f8-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="d69f8-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d69f8-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


