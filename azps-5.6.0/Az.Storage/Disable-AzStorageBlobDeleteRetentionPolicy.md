---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f4ffd20a835a8357972c9f8b9209d505fd311c1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929362"
---
# <span data-ttu-id="e4816-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e4816-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="e4816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4816-102">SYNOPSIS</span></span>
<span data-ttu-id="e4816-103">Tiltsa le az Azure Storage Blob szolgáltatás törlési adatmegőrzési házirendét.</span><span class="sxs-lookup"><span data-stu-id="e4816-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="e4816-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e4816-104">SYNTAX</span></span>

### <span data-ttu-id="e4816-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4816-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4816-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e4816-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4816-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="e4816-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4816-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e4816-108">DESCRIPTION</span></span>
<span data-ttu-id="e4816-109">A **Disable-AzStorageBlobDeleteRetentionPolicy parancsmag** letiltja az Azure Storage Blob szolgáltatás törlési adatmegőrzési házirendét.</span><span class="sxs-lookup"><span data-stu-id="e4816-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="e4816-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e4816-110">EXAMPLES</span></span>

### <span data-ttu-id="e4816-111">1. példa: A Blob szolgáltatás törlési adatmegőrzési házirendének letiltása</span><span class="sxs-lookup"><span data-stu-id="e4816-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="e4816-112">Ez a parancs letiltja a Blob szolgáltatás törlési adatmegőrzési házirendét.</span><span class="sxs-lookup"><span data-stu-id="e4816-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="e4816-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4816-113">PARAMETERS</span></span>

### <span data-ttu-id="e4816-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4816-114">-DefaultProfile</span></span>
<span data-ttu-id="e4816-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4816-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4816-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4816-116">-PassThru</span></span>
<span data-ttu-id="e4816-117">Display ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="e4816-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="e4816-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4816-118">-ResourceGroupName</span></span>
<span data-ttu-id="e4816-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e4816-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="e4816-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4816-120">-ResourceId</span></span>
<span data-ttu-id="e4816-121">Adja meg a tárfiók erőforrás-azonosítóját vagy a Blob szolgáltatás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="e4816-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="e4816-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4816-122">-StorageAccount</span></span>
<span data-ttu-id="e4816-123">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="e4816-123">Storage account object</span></span>

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

### <span data-ttu-id="e4816-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e4816-124">-StorageAccountName</span></span>
<span data-ttu-id="e4816-125">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="e4816-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="e4816-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4816-126">-Confirm</span></span>
<span data-ttu-id="e4816-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e4816-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4816-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4816-128">-WhatIf</span></span>
<span data-ttu-id="e4816-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e4816-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4816-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4816-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4816-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4816-131">CommonParameters</span></span>
<span data-ttu-id="e4816-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4816-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4816-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4816-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4816-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4816-134">INPUTS</span></span>

### <span data-ttu-id="e4816-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4816-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e4816-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e4816-136">System.String</span></span>

## <span data-ttu-id="e4816-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4816-137">OUTPUTS</span></span>

### <span data-ttu-id="e4816-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e4816-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="e4816-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e4816-139">NOTES</span></span>

## <span data-ttu-id="e4816-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4816-140">RELATED LINKS</span></span>
