---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f8303a9d87a2bd5312732bd01eb3d42bd1e0a285
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493305"
---
# <span data-ttu-id="479a9-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="479a9-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="479a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="479a9-102">SYNOPSIS</span></span>
<span data-ttu-id="479a9-103">Engedélyezze az Azure Storage blob szolgáltatás adatmegőrzési házirendjének törlését.</span><span class="sxs-lookup"><span data-stu-id="479a9-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="479a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="479a9-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="479a9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="479a9-105">DESCRIPTION</span></span>
<span data-ttu-id="479a9-106">Az **enable-AzureStorageDeleteRetentionPolicy** parancsmag az Azure Storage blob szolgáltatás adatmegőrzési házirendjének törlését teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="479a9-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="479a9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="479a9-107">EXAMPLES</span></span>

### <span data-ttu-id="479a9-108">Példa 1: a blob-szolgáltatás adatmegőrzési házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="479a9-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="479a9-109">Ez a parancs engedélyezi a blob-szolgáltatás adatmegőrzési házirendjét, és a törölt blob-adatmegőrzési napokat a 3 értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="479a9-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="479a9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="479a9-110">PARAMETERS</span></span>

### <span data-ttu-id="479a9-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="479a9-111">-Context</span></span>
<span data-ttu-id="479a9-112">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="479a9-112">Azure Storage Context Object</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="479a9-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="479a9-113">-PassThru</span></span>
<span data-ttu-id="479a9-114">DeleteRetentionPolicyProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="479a9-114">Display DeleteRetentionPolicyProperties</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="479a9-115">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="479a9-115">-RetentionDays</span></span>
<span data-ttu-id="479a9-116">Megadja a DeleteRetentionPolicy retenciós napjainak számát.</span><span class="sxs-lookup"><span data-stu-id="479a9-116">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="479a9-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="479a9-117">-Confirm</span></span>
<span data-ttu-id="479a9-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="479a9-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="479a9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="479a9-119">-WhatIf</span></span>
<span data-ttu-id="479a9-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="479a9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="479a9-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="479a9-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="479a9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="479a9-122">CommonParameters</span></span>
<span data-ttu-id="479a9-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="479a9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="479a9-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="479a9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="479a9-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="479a9-125">INPUTS</span></span>

### <span data-ttu-id="479a9-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="479a9-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="479a9-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="479a9-127">OUTPUTS</span></span>

### <span data-ttu-id="479a9-128">Microsoft. WindowsAzure. Storage. Shared. Protocol. DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="479a9-128">Microsoft.WindowsAzure.Storage.Shared.Protocol.DeleteRetentionPolicyProperties</span></span>

## <span data-ttu-id="479a9-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="479a9-129">NOTES</span></span>

## <span data-ttu-id="479a9-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="479a9-130">RELATED LINKS</span></span>

