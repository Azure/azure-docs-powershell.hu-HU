---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011259"
---
# <span data-ttu-id="e4116-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e4116-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="e4116-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4116-102">SYNOPSIS</span></span>
<span data-ttu-id="e4116-103">Tiltsa le a törlés adatmegőrzési házirendet az Azure Storage blob szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e4116-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="e4116-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4116-104">SYNTAX</span></span>

### <span data-ttu-id="e4116-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e4116-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4116-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e4116-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4116-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="e4116-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4116-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4116-108">DESCRIPTION</span></span>
<span data-ttu-id="e4116-109">A **disable-AzStorageBlobDeleteRetentionPolicy** parancsmag letiltja a törlés-adatmegőrzési házirendet az Azure Storage blob szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="e4116-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="e4116-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e4116-110">EXAMPLES</span></span>

### <span data-ttu-id="e4116-111">1. példa: a blob-szolgáltatás adatmegőrzési házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="e4116-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="e4116-112">Ez a parancs letiltja a blob-szolgáltatás adatmegőrzési házirendjének törlését.</span><span class="sxs-lookup"><span data-stu-id="e4116-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="e4116-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4116-113">PARAMETERS</span></span>

### <span data-ttu-id="e4116-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4116-114">-DefaultProfile</span></span>
<span data-ttu-id="e4116-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4116-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4116-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4116-116">-PassThru</span></span>
<span data-ttu-id="e4116-117">ServiceProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="e4116-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="e4116-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4116-118">-ResourceGroupName</span></span>
<span data-ttu-id="e4116-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e4116-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="e4116-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4116-120">-ResourceId</span></span>
<span data-ttu-id="e4116-121">Adja meg a tárolási fiók erőforrás-azonosítóját vagy a blob-szolgáltatás tulajdonságainak erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="e4116-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="e4116-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4116-122">-StorageAccount</span></span>
<span data-ttu-id="e4116-123">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="e4116-123">Storage account object</span></span>

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

### <span data-ttu-id="e4116-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e4116-124">-StorageAccountName</span></span>
<span data-ttu-id="e4116-125">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="e4116-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="e4116-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4116-126">-Confirm</span></span>
<span data-ttu-id="e4116-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e4116-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4116-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4116-128">-WhatIf</span></span>
<span data-ttu-id="e4116-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e4116-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4116-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4116-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4116-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4116-131">CommonParameters</span></span>
<span data-ttu-id="e4116-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4116-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4116-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4116-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4116-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4116-134">INPUTS</span></span>

### <span data-ttu-id="e4116-135">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e4116-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e4116-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e4116-136">System.String</span></span>

## <span data-ttu-id="e4116-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4116-137">OUTPUTS</span></span>

### <span data-ttu-id="e4116-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e4116-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="e4116-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4116-139">NOTES</span></span>

## <span data-ttu-id="e4116-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4116-140">RELATED LINKS</span></span>
