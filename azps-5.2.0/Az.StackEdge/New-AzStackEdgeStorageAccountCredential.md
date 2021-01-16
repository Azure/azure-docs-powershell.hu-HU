---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: d4e9062b15e7d5ca7338e13cdcdf71506ba23e29
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352301"
---
# <span data-ttu-id="40e25-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="40e25-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="40e25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40e25-102">SYNOPSIS</span></span>
<span data-ttu-id="40e25-103">Új hitelesítő adatokat hoz létre egy edge storage-fiókhoz az eszközön.</span><span class="sxs-lookup"><span data-stu-id="40e25-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="40e25-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40e25-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40e25-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40e25-105">DESCRIPTION</span></span>
<span data-ttu-id="40e25-106">A **New-AzStackEdgeStorageAccountCredential** parancsmag létrehoz egy új, a Stack Edge-et tároló eszközhöz szükséges hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="40e25-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="40e25-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40e25-107">EXAMPLES</span></span>

### <span data-ttu-id="40e25-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="40e25-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="40e25-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40e25-109">PARAMETERS</span></span>

### <span data-ttu-id="40e25-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40e25-110">-AsJob</span></span>
<span data-ttu-id="40e25-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="40e25-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40e25-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e25-112">-DefaultProfile</span></span>
<span data-ttu-id="40e25-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40e25-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40e25-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="40e25-114">-DeviceName</span></span>
<span data-ttu-id="40e25-115">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="40e25-115">Device Name</span></span>

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

### <span data-ttu-id="40e25-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="40e25-116">-EncryptionKey</span></span>
<span data-ttu-id="40e25-117">A Edge-eszköz titkosítási kulcsa</span><span class="sxs-lookup"><span data-stu-id="40e25-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="40e25-118">-Name</span><span class="sxs-lookup"><span data-stu-id="40e25-118">-Name</span></span>
<span data-ttu-id="40e25-119">A használni használt tárfiók neve</span><span class="sxs-lookup"><span data-stu-id="40e25-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e25-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e25-120">-ResourceGroupName</span></span>
<span data-ttu-id="40e25-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="40e25-121">Resource Group Name</span></span>

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

### <span data-ttu-id="40e25-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="40e25-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="40e25-123">tárfiók hozzáférési kulcsának létrehozása</span><span class="sxs-lookup"><span data-stu-id="40e25-123">provide storage account access key</span></span>

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

### <span data-ttu-id="40e25-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="40e25-124">-StorageAccountType</span></span>
<span data-ttu-id="40e25-125">Lehetséges Tárterület-elérés típusa GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="40e25-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="40e25-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40e25-126">-Confirm</span></span>
<span data-ttu-id="40e25-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="40e25-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40e25-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e25-128">-WhatIf</span></span>
<span data-ttu-id="40e25-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="40e25-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40e25-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40e25-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40e25-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e25-131">CommonParameters</span></span>
<span data-ttu-id="40e25-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e25-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e25-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40e25-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e25-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40e25-134">INPUTS</span></span>

### <span data-ttu-id="40e25-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="40e25-135">None</span></span>

## <span data-ttu-id="40e25-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40e25-136">OUTPUTS</span></span>

### <span data-ttu-id="40e25-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="40e25-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="40e25-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40e25-138">NOTES</span></span>

## <span data-ttu-id="40e25-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40e25-139">RELATED LINKS</span></span>
