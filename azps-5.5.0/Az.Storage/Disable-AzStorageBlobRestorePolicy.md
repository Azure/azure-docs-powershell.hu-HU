---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156107"
---
# <span data-ttu-id="0e4cb-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="0e4cb-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="0e4cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e4cb-102">SYNOPSIS</span></span>
<span data-ttu-id="0e4cb-103">Letiltja a blob-visszaállítási házirendet egy tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="0e4cb-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="0e4cb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0e4cb-104">SYNTAX</span></span>

### <span data-ttu-id="0e4cb-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e4cb-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e4cb-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0e4cb-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e4cb-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="0e4cb-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e4cb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0e4cb-108">DESCRIPTION</span></span>
<span data-ttu-id="0e4cb-109">A **Disable-AzStorageBlobRestorePolicy** parancsmag letiltja a blob-visszaállítási házirendet az Azure Storage Blob szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="0e4cb-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="0e4cb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0e4cb-110">EXAMPLES</span></span>

### <span data-ttu-id="0e4cb-111">1. példa: Az Azure Storage Blob szolgáltatás blob-visszaállítási házirendének letiltása tárfiókon</span><span class="sxs-lookup"><span data-stu-id="0e4cb-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="0e4cb-112">Ez a parancs letiltja a blob-visszaállítási házirendet egy tárfiók Azure Storage Blob szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="0e4cb-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="0e4cb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e4cb-113">PARAMETERS</span></span>

### <span data-ttu-id="0e4cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e4cb-114">-DefaultProfile</span></span>
<span data-ttu-id="0e4cb-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e4cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e4cb-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e4cb-116">-PassThru</span></span>
<span data-ttu-id="0e4cb-117">Display ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="0e4cb-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="0e4cb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e4cb-118">-ResourceGroupName</span></span>
<span data-ttu-id="0e4cb-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0e4cb-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="0e4cb-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e4cb-120">-ResourceId</span></span>
<span data-ttu-id="0e4cb-121">Adja meg a tárfiók erőforrás-azonosítóját vagy a Blob szolgáltatás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="0e4cb-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="0e4cb-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e4cb-122">-StorageAccount</span></span>
<span data-ttu-id="0e4cb-123">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="0e4cb-123">Storage account object</span></span>

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

### <span data-ttu-id="0e4cb-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0e4cb-124">-StorageAccountName</span></span>
<span data-ttu-id="0e4cb-125">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="0e4cb-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="0e4cb-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e4cb-126">-Confirm</span></span>
<span data-ttu-id="0e4cb-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0e4cb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e4cb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e4cb-128">-WhatIf</span></span>
<span data-ttu-id="0e4cb-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0e4cb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e4cb-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e4cb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e4cb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e4cb-131">CommonParameters</span></span>
<span data-ttu-id="0e4cb-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e4cb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e4cb-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e4cb-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e4cb-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e4cb-134">INPUTS</span></span>

### <span data-ttu-id="0e4cb-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e4cb-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0e4cb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0e4cb-136">System.String</span></span>

## <span data-ttu-id="0e4cb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e4cb-137">OUTPUTS</span></span>

### <span data-ttu-id="0e4cb-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="0e4cb-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="0e4cb-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0e4cb-139">NOTES</span></span>

## <span data-ttu-id="0e4cb-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e4cb-140">RELATED LINKS</span></span>
