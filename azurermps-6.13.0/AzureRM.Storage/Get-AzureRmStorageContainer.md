---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
ms.openlocfilehash: 64e3857ddd9a9bb00b94e3e550c6be33722990a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492697"
---
# <span data-ttu-id="96dd6-101">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="96dd6-101">Get-AzureRmStorageContainer</span></span>

## <span data-ttu-id="96dd6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="96dd6-103">Tároló blob-tárolók beolvasása vagy listázása</span><span class="sxs-lookup"><span data-stu-id="96dd6-103">Gets or lists Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96dd6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96dd6-104">SYNTAX</span></span>

### <span data-ttu-id="96dd6-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="96dd6-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96dd6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="96dd6-106">AccountObject</span></span>
```
Get-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96dd6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="96dd6-107">DESCRIPTION</span></span>
<span data-ttu-id="96dd6-108">A **Get-AzureRmStorageContainer** parancsmag tároló blob-tárolókat kap vagy listáz</span><span class="sxs-lookup"><span data-stu-id="96dd6-108">The **Get-AzureRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="96dd6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="96dd6-109">EXAMPLES</span></span>

### <span data-ttu-id="96dd6-110">Példa 1: tároló blob-tároló beszerzése tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="96dd6-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" 
```

<span data-ttu-id="96dd6-111">Ez a parancs a tároló blob-tárolóját a tárolási fiók nevével és a tároló nevével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="96dd6-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="96dd6-112">2. példa: a tárolási fiók minden tároló blob-tárolójának listázása</span><span class="sxs-lookup"><span data-stu-id="96dd6-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" 
```

<span data-ttu-id="96dd6-113">Ez a parancs felsorolja az összes tárterület-tároló blob-tárolóját a tárolási fiók nevével.</span><span class="sxs-lookup"><span data-stu-id="96dd6-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="96dd6-114">3. példa: adattároló blob-tároló beszerzése tárolási fiók objektummal és tároló nevével</span><span class="sxs-lookup"><span data-stu-id="96dd6-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" 
```

<span data-ttu-id="96dd6-115">Ez a parancs egy tároló BLOB-tárolót kap a Storage Account objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="96dd6-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="96dd6-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96dd6-116">PARAMETERS</span></span>

### <span data-ttu-id="96dd6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96dd6-117">-DefaultProfile</span></span>
<span data-ttu-id="96dd6-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96dd6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96dd6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96dd6-119">-Name</span></span>
<span data-ttu-id="96dd6-120">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="96dd6-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96dd6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96dd6-121">-ResourceGroupName</span></span>
<span data-ttu-id="96dd6-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="96dd6-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96dd6-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="96dd6-123">-StorageAccount</span></span>
<span data-ttu-id="96dd6-124">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="96dd6-124">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96dd6-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="96dd6-125">-StorageAccountName</span></span>
<span data-ttu-id="96dd6-126">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="96dd6-126">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96dd6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96dd6-127">CommonParameters</span></span>
<span data-ttu-id="96dd6-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96dd6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96dd6-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96dd6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96dd6-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96dd6-130">INPUTS</span></span>

### <span data-ttu-id="96dd6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="96dd6-131">System.String</span></span>

## <span data-ttu-id="96dd6-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96dd6-132">OUTPUTS</span></span>

### <span data-ttu-id="96dd6-133">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="96dd6-133">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="96dd6-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96dd6-134">NOTES</span></span>

## <span data-ttu-id="96dd6-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96dd6-135">RELATED LINKS</span></span>

