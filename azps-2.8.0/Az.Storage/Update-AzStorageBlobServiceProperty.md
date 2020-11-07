---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 195bc966bb47bf921eb0150272cfb9af6d73c63a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839615"
---
# <span data-ttu-id="b9e57-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b9e57-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="b9e57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9e57-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e57-103">Módosítja az Azure Storage blob szolgáltatás szolgáltatás tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="b9e57-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b9e57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9e57-104">SYNTAX</span></span>

### <span data-ttu-id="b9e57-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9e57-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9e57-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b9e57-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e57-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="b9e57-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e57-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9e57-108">DESCRIPTION</span></span>
<span data-ttu-id="b9e57-109">Az **Update-AzStorageBlobServiceProperty** parancsmag módosítja az Azure Storage blob szolgáltatás tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="b9e57-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b9e57-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b9e57-110">EXAMPLES</span></span>

### <span data-ttu-id="b9e57-111">1. példa: a blob-szolgáltatás DefaultServiceVersion beállítása az 2018-03-28-be</span><span class="sxs-lookup"><span data-stu-id="b9e57-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False
```

<span data-ttu-id="b9e57-112">Ez a parancs a blob-szolgáltatás DefaultServiceVersion a 2018-03-28-ra állítja be.</span><span class="sxs-lookup"><span data-stu-id="b9e57-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="b9e57-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9e57-113">PARAMETERS</span></span>

### <span data-ttu-id="b9e57-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e57-114">-DefaultProfile</span></span>
<span data-ttu-id="b9e57-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9e57-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9e57-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="b9e57-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="b9e57-117">A beállítani kívánt alapértelmezett szolgáltatási verzió</span><span class="sxs-lookup"><span data-stu-id="b9e57-117">Default Service Version to Set</span></span>

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

### <span data-ttu-id="b9e57-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e57-118">-ResourceGroupName</span></span>
<span data-ttu-id="b9e57-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b9e57-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="b9e57-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9e57-120">-ResourceId</span></span>
<span data-ttu-id="b9e57-121">Adja meg a tárolási fiók erőforrás-azonosítóját vagy a blob-szolgáltatás tulajdonságainak erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="b9e57-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="b9e57-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b9e57-122">-StorageAccount</span></span>
<span data-ttu-id="b9e57-123">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="b9e57-123">Storage account object</span></span>

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

### <span data-ttu-id="b9e57-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b9e57-124">-StorageAccountName</span></span>
<span data-ttu-id="b9e57-125">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="b9e57-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="b9e57-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9e57-126">-Confirm</span></span>
<span data-ttu-id="b9e57-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9e57-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e57-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e57-128">-WhatIf</span></span>
<span data-ttu-id="b9e57-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9e57-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e57-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9e57-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e57-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e57-131">CommonParameters</span></span>
<span data-ttu-id="b9e57-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9e57-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e57-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e57-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e57-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9e57-134">INPUTS</span></span>

### <span data-ttu-id="b9e57-135">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b9e57-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b9e57-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b9e57-136">System.String</span></span>

## <span data-ttu-id="b9e57-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9e57-137">OUTPUTS</span></span>

### <span data-ttu-id="b9e57-138">Microsoft. Azure. Command. Management. Storage. models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="b9e57-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="b9e57-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9e57-139">NOTES</span></span>

## <span data-ttu-id="b9e57-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9e57-140">RELATED LINKS</span></span>
