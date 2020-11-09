---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300413"
---
# <span data-ttu-id="c1709-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1709-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="c1709-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1709-102">SYNOPSIS</span></span>
<span data-ttu-id="c1709-103">Tiltsa le a törlés adatmegőrzési házirendet az Azure Storage blob szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="c1709-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c1709-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1709-104">SYNTAX</span></span>

### <span data-ttu-id="c1709-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1709-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1709-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c1709-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1709-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="c1709-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1709-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1709-108">DESCRIPTION</span></span>
<span data-ttu-id="c1709-109">A **disable-AzStorageBlobDeleteRetentionPolicy** parancsmag letiltja a törlés-adatmegőrzési házirendet az Azure Storage blob szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="c1709-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c1709-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c1709-110">EXAMPLES</span></span>

### <span data-ttu-id="c1709-111">1. példa: a blob-szolgáltatás adatmegőrzési házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="c1709-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="c1709-112">Ez a parancs letiltja a blob-szolgáltatás adatmegőrzési házirendjének törlését.</span><span class="sxs-lookup"><span data-stu-id="c1709-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="c1709-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1709-113">PARAMETERS</span></span>

### <span data-ttu-id="c1709-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1709-114">-DefaultProfile</span></span>
<span data-ttu-id="c1709-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1709-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1709-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1709-116">-PassThru</span></span>
<span data-ttu-id="c1709-117">ServiceProperties megjelenítése</span><span class="sxs-lookup"><span data-stu-id="c1709-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="c1709-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1709-118">-ResourceGroupName</span></span>
<span data-ttu-id="c1709-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c1709-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="c1709-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1709-120">-ResourceId</span></span>
<span data-ttu-id="c1709-121">Adja meg a tárolási fiók erőforrás-azonosítóját vagy a blob-szolgáltatás tulajdonságainak erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="c1709-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="c1709-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1709-122">-StorageAccount</span></span>
<span data-ttu-id="c1709-123">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="c1709-123">Storage account object</span></span>

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

### <span data-ttu-id="c1709-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c1709-124">-StorageAccountName</span></span>
<span data-ttu-id="c1709-125">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="c1709-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="c1709-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1709-126">-Confirm</span></span>
<span data-ttu-id="c1709-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1709-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1709-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1709-128">-WhatIf</span></span>
<span data-ttu-id="c1709-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1709-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1709-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1709-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1709-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1709-131">CommonParameters</span></span>
<span data-ttu-id="c1709-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1709-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1709-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1709-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1709-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1709-134">INPUTS</span></span>

### <span data-ttu-id="c1709-135">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1709-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c1709-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c1709-136">System.String</span></span>

## <span data-ttu-id="c1709-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1709-137">OUTPUTS</span></span>

### <span data-ttu-id="c1709-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1709-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="c1709-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1709-139">NOTES</span></span>

## <span data-ttu-id="c1709-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1709-140">RELATED LINKS</span></span>
