---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 7cdef2f35180712d0751149a85e4a422a868c389
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195099"
---
# <span data-ttu-id="f5814-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f5814-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="f5814-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5814-102">SYNOPSIS</span></span>
<span data-ttu-id="f5814-103">Az Azure Storage blob Services szolgáltatás tulajdonságainak beolvasása.</span><span class="sxs-lookup"><span data-stu-id="f5814-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="f5814-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5814-104">SYNTAX</span></span>

### <span data-ttu-id="f5814-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5814-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5814-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f5814-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5814-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="f5814-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5814-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5814-108">DESCRIPTION</span></span>
<span data-ttu-id="f5814-109">A **Get-AzStorageBlobServiceProperty** parancsmag az Azure Storage blob Services szolgáltatás tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f5814-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="f5814-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f5814-110">EXAMPLES</span></span>

### <span data-ttu-id="f5814-111">Példa 1: az Azure Storage blob Services tulajdonság beszerzése egy megadott tárterület-fiókból</span><span class="sxs-lookup"><span data-stu-id="f5814-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="f5814-112">Ez a parancs egy megadott tárterület-fiók blob Services tulajdonságát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f5814-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="f5814-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5814-113">PARAMETERS</span></span>

### <span data-ttu-id="f5814-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5814-114">-DefaultProfile</span></span>
<span data-ttu-id="f5814-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5814-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5814-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5814-116">-ResourceGroupName</span></span>
<span data-ttu-id="f5814-117">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f5814-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="f5814-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5814-118">-ResourceId</span></span>
<span data-ttu-id="f5814-119">BLOB-szolgáltatás tulajdonságai – erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f5814-119">Blob Service Properties Resource Id.</span></span>

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

### <span data-ttu-id="f5814-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5814-120">-StorageAccount</span></span>
<span data-ttu-id="f5814-121">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="f5814-121">Storage account object</span></span>

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

### <span data-ttu-id="f5814-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f5814-122">-StorageAccountName</span></span>
<span data-ttu-id="f5814-123">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f5814-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="f5814-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5814-124">CommonParameters</span></span>
<span data-ttu-id="f5814-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5814-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5814-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5814-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5814-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5814-127">INPUTS</span></span>

### <span data-ttu-id="f5814-128">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5814-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f5814-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f5814-129">System.String</span></span>

## <span data-ttu-id="f5814-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5814-130">OUTPUTS</span></span>

### <span data-ttu-id="f5814-131">Microsoft. Azure. Command. Management. Storage. models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="f5814-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="f5814-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5814-132">NOTES</span></span>

## <span data-ttu-id="f5814-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5814-133">RELATED LINKS</span></span>
