---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: b7d6299af3f56dd8f09c73171ab6630cbbb9bc96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012524"
---
# <span data-ttu-id="8c93f-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8c93f-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="8c93f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c93f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c93f-103">Módosítja az Azure Storage blob szolgáltatás szolgáltatás tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="8c93f-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8c93f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c93f-104">SYNTAX</span></span>

### <span data-ttu-id="8c93f-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c93f-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c93f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8c93f-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c93f-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="8c93f-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c93f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c93f-108">DESCRIPTION</span></span>
<span data-ttu-id="8c93f-109">Az **Update-AzStorageBlobServiceProperty** parancsmag módosítja az Azure Storage blob szolgáltatás tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="8c93f-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8c93f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8c93f-110">EXAMPLES</span></span>

### <span data-ttu-id="8c93f-111">1. példa: a blob-szolgáltatás DefaultServiceVersion beállítása az 2018-03-28-be</span><span class="sxs-lookup"><span data-stu-id="8c93f-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False                                                   
```

<span data-ttu-id="8c93f-112">Ez a parancs a blob-szolgáltatás DefaultServiceVersion a 2018-03-28-ra állítja be.</span><span class="sxs-lookup"><span data-stu-id="8c93f-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="8c93f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c93f-113">PARAMETERS</span></span>

### <span data-ttu-id="8c93f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c93f-114">-DefaultProfile</span></span>
<span data-ttu-id="8c93f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c93f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c93f-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="8c93f-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="8c93f-117">A beállítani kívánt alapértelmezett szolgáltatási verzió</span><span class="sxs-lookup"><span data-stu-id="8c93f-117">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c93f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c93f-118">-ResourceGroupName</span></span>
<span data-ttu-id="8c93f-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8c93f-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="8c93f-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c93f-120">-ResourceId</span></span>
<span data-ttu-id="8c93f-121">Adja meg a tárolási fiók erőforrás-azonosítóját vagy a blob-szolgáltatás tulajdonságainak erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="8c93f-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="8c93f-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c93f-122">-StorageAccount</span></span>
<span data-ttu-id="8c93f-123">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="8c93f-123">Storage account object</span></span>

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

### <span data-ttu-id="8c93f-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8c93f-124">-StorageAccountName</span></span>
<span data-ttu-id="8c93f-125">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="8c93f-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="8c93f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8c93f-126">-Confirm</span></span>
<span data-ttu-id="8c93f-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c93f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c93f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c93f-128">-WhatIf</span></span>
<span data-ttu-id="8c93f-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8c93f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c93f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c93f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c93f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c93f-131">CommonParameters</span></span>
<span data-ttu-id="8c93f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c93f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c93f-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c93f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c93f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c93f-134">INPUTS</span></span>

### <span data-ttu-id="8c93f-135">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c93f-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8c93f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8c93f-136">System.String</span></span>

## <span data-ttu-id="8c93f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c93f-137">OUTPUTS</span></span>

### <span data-ttu-id="8c93f-138">Microsoft. Azure. Command. Management. Storage. models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="8c93f-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="8c93f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c93f-139">NOTES</span></span>

## <span data-ttu-id="8c93f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c93f-140">RELATED LINKS</span></span>
