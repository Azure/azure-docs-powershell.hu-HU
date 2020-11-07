---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: fdac081aa6edc5ac43c98800ad2d857cb8f62b09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668695"
---
# <span data-ttu-id="0cf18-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0cf18-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="0cf18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0cf18-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf18-103">Engedélyezze az Azure Storage blob szolgáltatás adatmegőrzési házirendjének törlését.</span><span class="sxs-lookup"><span data-stu-id="0cf18-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="0cf18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0cf18-104">SYNTAX</span></span>

### <span data-ttu-id="0cf18-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0cf18-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0cf18-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0cf18-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cf18-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="0cf18-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cf18-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0cf18-108">DESCRIPTION</span></span>
<span data-ttu-id="0cf18-109">Az **enable-AzStorageBlobDeleteRetentionPolicy** parancsmag az Azure Storage blob szolgáltatás adatmegőrzési házirendjének törlését teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="0cf18-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="0cf18-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0cf18-110">EXAMPLES</span></span>

### <span data-ttu-id="0cf18-111">Példa 1: a blob-szolgáltatás adatmegőrzési házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="0cf18-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="0cf18-112">Ez a parancs engedélyezi a blob-szolgáltatás adatmegőrzési házirendjét, és beállítja a törölt blob-adatmegőrzési napokat 4-ra.</span><span class="sxs-lookup"><span data-stu-id="0cf18-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="0cf18-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0cf18-113">PARAMETERS</span></span>

### <span data-ttu-id="0cf18-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf18-114">-DefaultProfile</span></span>
<span data-ttu-id="0cf18-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cf18-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cf18-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cf18-116">-PassThru</span></span>
<span data-ttu-id="0cf18-117">ServiceProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="0cf18-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="0cf18-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cf18-118">-ResourceGroupName</span></span>
<span data-ttu-id="0cf18-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="0cf18-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="0cf18-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cf18-120">-ResourceId</span></span>
<span data-ttu-id="0cf18-121">Adja meg a tárolási fiók erőforrás-azonosítóját vagy a blob-szolgáltatás tulajdonságainak erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="0cf18-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="0cf18-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="0cf18-122">-RetentionDays</span></span>
<span data-ttu-id="0cf18-123">Megadja a DeleteRetentionPolicy retenciós napjainak számát.</span><span class="sxs-lookup"><span data-stu-id="0cf18-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="0cf18-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0cf18-124">-StorageAccount</span></span>
<span data-ttu-id="0cf18-125">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="0cf18-125">Storage account object</span></span>

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

### <span data-ttu-id="0cf18-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0cf18-126">-StorageAccountName</span></span>
<span data-ttu-id="0cf18-127">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="0cf18-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="0cf18-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0cf18-128">-Confirm</span></span>
<span data-ttu-id="0cf18-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0cf18-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cf18-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cf18-130">-WhatIf</span></span>
<span data-ttu-id="0cf18-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0cf18-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cf18-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0cf18-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cf18-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf18-133">CommonParameters</span></span>
<span data-ttu-id="0cf18-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0cf18-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf18-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cf18-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf18-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cf18-136">INPUTS</span></span>

### <span data-ttu-id="0cf18-137">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0cf18-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0cf18-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0cf18-138">System.String</span></span>

## <span data-ttu-id="0cf18-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cf18-139">OUTPUTS</span></span>

### <span data-ttu-id="0cf18-140">Microsoft. Azure. Command. Management. Storage. models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="0cf18-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="0cf18-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0cf18-141">NOTES</span></span>

## <span data-ttu-id="0cf18-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cf18-142">RELATED LINKS</span></span>
