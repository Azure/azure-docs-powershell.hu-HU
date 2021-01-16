---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374162"
---
# <span data-ttu-id="40d30-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="40d30-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="40d30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40d30-102">SYNOPSIS</span></span>
<span data-ttu-id="40d30-103">Tiltsa le az Azure Storage Blob szolgáltatás törlési adatmegőrzési házirendét.</span><span class="sxs-lookup"><span data-stu-id="40d30-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="40d30-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40d30-104">SYNTAX</span></span>

### <span data-ttu-id="40d30-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40d30-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d30-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="40d30-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d30-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="40d30-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d30-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40d30-108">DESCRIPTION</span></span>
<span data-ttu-id="40d30-109">A **Disable-AzStorageBlobDeleteRetentionPolicy parancsmag** letiltja az Azure Storage Blob szolgáltatás törlési adatmegőrzési házirendét.</span><span class="sxs-lookup"><span data-stu-id="40d30-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="40d30-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40d30-110">EXAMPLES</span></span>

### <span data-ttu-id="40d30-111">1. példa: A Blob szolgáltatás törlési adatmegőrzési házirendének letiltása</span><span class="sxs-lookup"><span data-stu-id="40d30-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="40d30-112">Ez a parancs letiltja a Blob szolgáltatás törlési adatmegőrzési házirendét.</span><span class="sxs-lookup"><span data-stu-id="40d30-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="40d30-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40d30-113">PARAMETERS</span></span>

### <span data-ttu-id="40d30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d30-114">-DefaultProfile</span></span>
<span data-ttu-id="40d30-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40d30-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40d30-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40d30-116">-PassThru</span></span>
<span data-ttu-id="40d30-117">Display ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="40d30-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="40d30-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d30-118">-ResourceGroupName</span></span>
<span data-ttu-id="40d30-119">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="40d30-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="40d30-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40d30-120">-ResourceId</span></span>
<span data-ttu-id="40d30-121">Adja meg a tárfiók erőforrás-azonosítóját vagy a Blob szolgáltatás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="40d30-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="40d30-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="40d30-122">-StorageAccount</span></span>
<span data-ttu-id="40d30-123">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="40d30-123">Storage account object</span></span>

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

### <span data-ttu-id="40d30-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="40d30-124">-StorageAccountName</span></span>
<span data-ttu-id="40d30-125">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="40d30-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="40d30-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40d30-126">-Confirm</span></span>
<span data-ttu-id="40d30-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="40d30-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d30-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d30-128">-WhatIf</span></span>
<span data-ttu-id="40d30-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="40d30-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d30-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40d30-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d30-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d30-131">CommonParameters</span></span>
<span data-ttu-id="40d30-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d30-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d30-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d30-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d30-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40d30-134">INPUTS</span></span>

### <span data-ttu-id="40d30-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="40d30-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="40d30-136">System.String</span><span class="sxs-lookup"><span data-stu-id="40d30-136">System.String</span></span>

## <span data-ttu-id="40d30-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40d30-137">OUTPUTS</span></span>

### <span data-ttu-id="40d30-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="40d30-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="40d30-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40d30-139">NOTES</span></span>

## <span data-ttu-id="40d30-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40d30-140">RELATED LINKS</span></span>
