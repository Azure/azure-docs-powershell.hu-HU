---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: b086703ba8466c6d67e297002e2127a092175c85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668698"
---
# <span data-ttu-id="f1c2f-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1c2f-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="f1c2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c2f-103">Tiltsa le a törlés adatmegőrzési házirendet az Azure Storage blob szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f1c2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1c2f-104">SYNTAX</span></span>

### <span data-ttu-id="f1c2f-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1c2f-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c2f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f1c2f-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c2f-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c2f-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1c2f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1c2f-108">DESCRIPTION</span></span>
<span data-ttu-id="f1c2f-109">A **disable-AzStorageBlobDeleteRetentionPolicy** parancsmag letiltja a törlés-adatmegőrzési házirendet az Azure Storage blob szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f1c2f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f1c2f-110">EXAMPLES</span></span>

### <span data-ttu-id="f1c2f-111">1. példa: a blob-szolgáltatás adatmegőrzési házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="f1c2f-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="f1c2f-112">Ez a parancs letiltja a blob-szolgáltatás adatmegőrzési házirendjének törlését.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="f1c2f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1c2f-113">PARAMETERS</span></span>

### <span data-ttu-id="f1c2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c2f-114">-DefaultProfile</span></span>
<span data-ttu-id="f1c2f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1c2f-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1c2f-116">-PassThru</span></span>
<span data-ttu-id="f1c2f-117">ServiceProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="f1c2f-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="f1c2f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c2f-118">-ResourceGroupName</span></span>
<span data-ttu-id="f1c2f-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="f1c2f-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c2f-120">-ResourceId</span></span>
<span data-ttu-id="f1c2f-121">Adja meg a tárolási fiók erőforrás-azonosítóját vagy a blob-szolgáltatás tulajdonságainak erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="f1c2f-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1c2f-122">-StorageAccount</span></span>
<span data-ttu-id="f1c2f-123">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="f1c2f-123">Storage account object</span></span>

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

### <span data-ttu-id="f1c2f-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f1c2f-124">-StorageAccountName</span></span>
<span data-ttu-id="f1c2f-125">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="f1c2f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1c2f-126">-Confirm</span></span>
<span data-ttu-id="f1c2f-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1c2f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1c2f-128">-WhatIf</span></span>
<span data-ttu-id="f1c2f-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1c2f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1c2f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c2f-131">CommonParameters</span></span>
<span data-ttu-id="f1c2f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1c2f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c2f-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1c2f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c2f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1c2f-134">INPUTS</span></span>

### <span data-ttu-id="f1c2f-135">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1c2f-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f1c2f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f1c2f-136">System.String</span></span>

## <span data-ttu-id="f1c2f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1c2f-137">OUTPUTS</span></span>

### <span data-ttu-id="f1c2f-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1c2f-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="f1c2f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1c2f-139">NOTES</span></span>

## <span data-ttu-id="f1c2f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1c2f-140">RELATED LINKS</span></span>
