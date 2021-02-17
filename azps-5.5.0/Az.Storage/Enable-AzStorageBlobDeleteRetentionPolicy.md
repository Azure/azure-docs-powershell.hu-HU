---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: ebb379217f9fd040aa3dcbd6c614a45dbdbba8c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207823"
---
# <span data-ttu-id="c9022-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c9022-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="c9022-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9022-102">SYNOPSIS</span></span>
<span data-ttu-id="c9022-103">Engedélyezze a törlési adatmegőrzési házirendet az Azure Storage Blob szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="c9022-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c9022-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c9022-104">SYNTAX</span></span>

### <span data-ttu-id="c9022-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9022-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9022-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c9022-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9022-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="c9022-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9022-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c9022-108">DESCRIPTION</span></span>
<span data-ttu-id="c9022-109">Az **Enable-AzStorageBlobDeleteRetentionPolicy parancsmag** törlési adatmegőrzési házirendet tesz lehetővé az Azure Storage Blob szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="c9022-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c9022-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c9022-110">EXAMPLES</span></span>

### <span data-ttu-id="c9022-111">1. példa: A Blob szolgáltatás törlési adatmegőrzési házirendének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="c9022-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="c9022-112">Ezzel a paranccsal törlési adatmegőrzési házirendet állíthat be a Blob szolgáltatásban, a törölt blobmegőrzési napokat pedig 4-re állíthatja.</span><span class="sxs-lookup"><span data-stu-id="c9022-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="c9022-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9022-113">PARAMETERS</span></span>

### <span data-ttu-id="c9022-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9022-114">-DefaultProfile</span></span>
<span data-ttu-id="c9022-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9022-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9022-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9022-116">-PassThru</span></span>
<span data-ttu-id="c9022-117">Display ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="c9022-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="c9022-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9022-118">-ResourceGroupName</span></span>
<span data-ttu-id="c9022-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c9022-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9022-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9022-120">-ResourceId</span></span>
<span data-ttu-id="c9022-121">Adja meg a tárfiók erőforrás-azonosítóját vagy a Blob szolgáltatás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="c9022-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9022-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="c9022-122">-RetentionDays</span></span>
<span data-ttu-id="c9022-123">Beállítja a DeleteRetentionPolicy adatmegőrzési napjainak számát.</span><span class="sxs-lookup"><span data-stu-id="c9022-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9022-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9022-124">-StorageAccount</span></span>
<span data-ttu-id="c9022-125">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="c9022-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9022-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c9022-126">-StorageAccountName</span></span>
<span data-ttu-id="c9022-127">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="c9022-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9022-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9022-128">-Confirm</span></span>
<span data-ttu-id="c9022-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c9022-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9022-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9022-130">-WhatIf</span></span>
<span data-ttu-id="c9022-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c9022-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9022-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9022-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9022-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9022-133">CommonParameters</span></span>
<span data-ttu-id="c9022-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9022-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9022-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9022-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9022-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9022-136">INPUTS</span></span>

### <span data-ttu-id="c9022-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9022-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c9022-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c9022-138">System.String</span></span>

## <span data-ttu-id="c9022-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9022-139">OUTPUTS</span></span>

### <span data-ttu-id="c9022-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="c9022-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="c9022-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c9022-141">NOTES</span></span>

## <span data-ttu-id="c9022-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9022-142">RELATED LINKS</span></span>
