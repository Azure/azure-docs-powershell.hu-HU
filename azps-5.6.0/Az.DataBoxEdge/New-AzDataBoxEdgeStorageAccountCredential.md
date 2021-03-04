---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 23fe08b273b95cd5ad3866437d131f432e6cee38
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931906"
---
# <span data-ttu-id="8c608-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8c608-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="8c608-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c608-102">SYNOPSIS</span></span>
<span data-ttu-id="8c608-103">Új hitelesítő adatokat hoz létre egy edge storage-fiókhoz az eszközön.</span><span class="sxs-lookup"><span data-stu-id="8c608-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="8c608-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c608-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c608-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c608-105">DESCRIPTION</span></span>
<span data-ttu-id="8c608-106">A **New-AzDataBoxEdgeStorageAccountCredential** parancsmag létrehoz egy új peremtárhelyfiók hitelesítő adatait egy Data Box Edge-eszközhöz.</span><span class="sxs-lookup"><span data-stu-id="8c608-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="8c608-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c608-107">EXAMPLES</span></span>

### <span data-ttu-id="8c608-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8c608-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="8c608-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c608-109">PARAMETERS</span></span>

### <span data-ttu-id="8c608-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c608-110">-AsJob</span></span>
<span data-ttu-id="8c608-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8c608-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c608-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c608-112">-DefaultProfile</span></span>
<span data-ttu-id="8c608-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c608-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c608-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8c608-114">-DeviceName</span></span>
<span data-ttu-id="8c608-115">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="8c608-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c608-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8c608-116">-EncryptionKey</span></span>
<span data-ttu-id="8c608-117">A Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="8c608-117">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c608-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8c608-118">-Name</span></span>
<span data-ttu-id="8c608-119">A használni használt tárfiók neve</span><span class="sxs-lookup"><span data-stu-id="8c608-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c608-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c608-120">-ResourceGroupName</span></span>
<span data-ttu-id="8c608-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8c608-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c608-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="8c608-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="8c608-123">tárfiók hozzáférési kulcsának létrehozása</span><span class="sxs-lookup"><span data-stu-id="8c608-123">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c608-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8c608-124">-StorageAccountType</span></span>
<span data-ttu-id="8c608-125">Lehetséges Tárterület-elérés típusa GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="8c608-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c608-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c608-126">-Confirm</span></span>
<span data-ttu-id="8c608-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c608-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c608-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c608-128">-WhatIf</span></span>
<span data-ttu-id="8c608-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c608-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c608-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c608-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c608-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c608-131">CommonParameters</span></span>
<span data-ttu-id="8c608-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c608-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c608-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c608-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c608-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c608-134">INPUTS</span></span>

### <span data-ttu-id="8c608-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="8c608-135">None</span></span>

## <span data-ttu-id="8c608-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c608-136">OUTPUTS</span></span>

### <span data-ttu-id="8c608-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8c608-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="8c608-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c608-138">NOTES</span></span>

## <span data-ttu-id="8c608-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c608-139">RELATED LINKS</span></span>
