---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 189b2860325ee95709139a402a9046f34e1f79d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929338"
---
# <span data-ttu-id="1d3c7-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="1d3c7-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="1d3c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d3c7-102">SYNOPSIS</span></span>
<span data-ttu-id="1d3c7-103">Letiltja a blob-visszaállítási házirendet egy tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="1d3c7-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="1d3c7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d3c7-104">SYNTAX</span></span>

### <span data-ttu-id="1d3c7-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d3c7-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d3c7-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1d3c7-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d3c7-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="1d3c7-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d3c7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d3c7-108">DESCRIPTION</span></span>
<span data-ttu-id="1d3c7-109">A **Disable-AzStorageBlobRestorePolicy** parancsmag letiltja a blob-visszaállítási házirendet az Azure Storage Blob szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="1d3c7-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="1d3c7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d3c7-110">EXAMPLES</span></span>

### <span data-ttu-id="1d3c7-111">1. példa: Az Azure Storage Blob szolgáltatás blob-visszaállítási házirendének letiltása tárfiókon</span><span class="sxs-lookup"><span data-stu-id="1d3c7-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="1d3c7-112">Ez a parancs letiltja a blob-visszaállítási házirendet egy tárfiók Azure Storage Blob szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="1d3c7-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="1d3c7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d3c7-113">PARAMETERS</span></span>

### <span data-ttu-id="1d3c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d3c7-114">-DefaultProfile</span></span>
<span data-ttu-id="1d3c7-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d3c7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d3c7-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d3c7-116">-PassThru</span></span>
<span data-ttu-id="1d3c7-117">Display ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="1d3c7-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="1d3c7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d3c7-118">-ResourceGroupName</span></span>
<span data-ttu-id="1d3c7-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1d3c7-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="1d3c7-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d3c7-120">-ResourceId</span></span>
<span data-ttu-id="1d3c7-121">Adja meg a tárfiók erőforrás-azonosítóját vagy a Blob szolgáltatás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="1d3c7-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="1d3c7-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d3c7-122">-StorageAccount</span></span>
<span data-ttu-id="1d3c7-123">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="1d3c7-123">Storage account object</span></span>

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

### <span data-ttu-id="1d3c7-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1d3c7-124">-StorageAccountName</span></span>
<span data-ttu-id="1d3c7-125">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="1d3c7-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="1d3c7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d3c7-126">-Confirm</span></span>
<span data-ttu-id="1d3c7-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1d3c7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d3c7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d3c7-128">-WhatIf</span></span>
<span data-ttu-id="1d3c7-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1d3c7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d3c7-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d3c7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d3c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d3c7-131">CommonParameters</span></span>
<span data-ttu-id="1d3c7-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d3c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d3c7-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d3c7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d3c7-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d3c7-134">INPUTS</span></span>

### <span data-ttu-id="1d3c7-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d3c7-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="1d3c7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1d3c7-136">System.String</span></span>

## <span data-ttu-id="1d3c7-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d3c7-137">OUTPUTS</span></span>

### <span data-ttu-id="1d3c7-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="1d3c7-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="1d3c7-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d3c7-139">NOTES</span></span>

## <span data-ttu-id="1d3c7-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d3c7-140">RELATED LINKS</span></span>
