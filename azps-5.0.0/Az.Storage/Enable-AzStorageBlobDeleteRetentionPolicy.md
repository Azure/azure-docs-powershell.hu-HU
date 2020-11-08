---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: ebb379217f9fd040aa3dcbd6c614a45dbdbba8c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195486"
---
# <span data-ttu-id="343e4-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="343e4-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="343e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="343e4-102">SYNOPSIS</span></span>
<span data-ttu-id="343e4-103">Engedélyezze az Azure Storage blob szolgáltatás adatmegőrzési házirendjének törlését.</span><span class="sxs-lookup"><span data-stu-id="343e4-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="343e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="343e4-104">SYNTAX</span></span>

### <span data-ttu-id="343e4-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="343e4-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="343e4-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="343e4-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="343e4-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="343e4-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="343e4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="343e4-108">DESCRIPTION</span></span>
<span data-ttu-id="343e4-109">Az **enable-AzStorageBlobDeleteRetentionPolicy** parancsmag az Azure Storage blob szolgáltatás adatmegőrzési házirendjének törlését teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="343e4-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="343e4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="343e4-110">EXAMPLES</span></span>

### <span data-ttu-id="343e4-111">Példa 1: a blob-szolgáltatás adatmegőrzési házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="343e4-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="343e4-112">Ez a parancs engedélyezi a blob-szolgáltatás adatmegőrzési házirendjét, és beállítja a törölt blob-adatmegőrzési napokat 4-ra.</span><span class="sxs-lookup"><span data-stu-id="343e4-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="343e4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="343e4-113">PARAMETERS</span></span>

### <span data-ttu-id="343e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343e4-114">-DefaultProfile</span></span>
<span data-ttu-id="343e4-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="343e4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="343e4-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="343e4-116">-PassThru</span></span>
<span data-ttu-id="343e4-117">ServiceProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="343e4-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="343e4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="343e4-118">-ResourceGroupName</span></span>
<span data-ttu-id="343e4-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="343e4-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="343e4-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="343e4-120">-ResourceId</span></span>
<span data-ttu-id="343e4-121">Adja meg a tárolási fiók erőforrás-azonosítóját vagy a blob-szolgáltatás tulajdonságainak erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="343e4-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="343e4-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="343e4-122">-RetentionDays</span></span>
<span data-ttu-id="343e4-123">Megadja a DeleteRetentionPolicy retenciós napjainak számát.</span><span class="sxs-lookup"><span data-stu-id="343e4-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="343e4-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="343e4-124">-StorageAccount</span></span>
<span data-ttu-id="343e4-125">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="343e4-125">Storage account object</span></span>

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

### <span data-ttu-id="343e4-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="343e4-126">-StorageAccountName</span></span>
<span data-ttu-id="343e4-127">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="343e4-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="343e4-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="343e4-128">-Confirm</span></span>
<span data-ttu-id="343e4-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="343e4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="343e4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="343e4-130">-WhatIf</span></span>
<span data-ttu-id="343e4-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="343e4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="343e4-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="343e4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="343e4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343e4-133">CommonParameters</span></span>
<span data-ttu-id="343e4-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="343e4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343e4-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="343e4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343e4-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="343e4-136">INPUTS</span></span>

### <span data-ttu-id="343e4-137">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="343e4-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="343e4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="343e4-138">System.String</span></span>

## <span data-ttu-id="343e4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="343e4-139">OUTPUTS</span></span>

### <span data-ttu-id="343e4-140">Microsoft. Azure. Command. Management. Storage. models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="343e4-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="343e4-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="343e4-141">NOTES</span></span>

## <span data-ttu-id="343e4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="343e4-142">RELATED LINKS</span></span>