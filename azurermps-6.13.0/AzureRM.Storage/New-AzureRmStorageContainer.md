---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
ms.openlocfilehash: 8e136188a2857b53b566d30c439e222caea16abb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492699"
---
# <span data-ttu-id="aed1c-101">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="aed1c-101">New-AzureRmStorageContainer</span></span>

## <span data-ttu-id="aed1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aed1c-102">SYNOPSIS</span></span>
<span data-ttu-id="aed1c-103">Tároló blob-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="aed1c-103">Creates a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aed1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aed1c-104">SYNTAX</span></span>

### <span data-ttu-id="aed1c-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aed1c-105">AccountName (Default)</span></span>
```
New-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aed1c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="aed1c-106">AccountObject</span></span>
```
New-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aed1c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aed1c-107">DESCRIPTION</span></span>
<span data-ttu-id="aed1c-108">A **New-AzureRmStorageContainer** parancsmag tároló BLOB-tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aed1c-108">The **New-AzureRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="aed1c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aed1c-109">EXAMPLES</span></span>

### <span data-ttu-id="aed1c-110">Példa 1: adattároló blob-tároló létrehozása a tárolási fiók nevével és a tároló nevével, metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="aed1c-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"} 
```

<span data-ttu-id="aed1c-111">Ez a parancs a tároló BLOB-tárolót hoz létre a tárolási fiók nevével és a tároló nevével, a metaadatokkal.</span><span class="sxs-lookup"><span data-stu-id="aed1c-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="aed1c-112">2. példa: adattároló blob-tároló létrehozása a tárolási fiók objektummal és a tároló nevével, a nyilvános hozzáférés blob-ként</span><span class="sxs-lookup"><span data-stu-id="aed1c-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="aed1c-113">Ez a parancs létrehoz egy tároló BLOB-tárolót a tárolási fiók objektummal és a tároló nevével, a nyilvános hozzáférés blob-ként.</span><span class="sxs-lookup"><span data-stu-id="aed1c-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="aed1c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aed1c-114">PARAMETERS</span></span>

### <span data-ttu-id="aed1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed1c-115">-DefaultProfile</span></span>
<span data-ttu-id="aed1c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aed1c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aed1c-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="aed1c-117">-Metadata</span></span>
<span data-ttu-id="aed1c-118">Tároló-metaadatok</span><span class="sxs-lookup"><span data-stu-id="aed1c-118">Container Metadata</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed1c-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aed1c-119">-Name</span></span>
<span data-ttu-id="aed1c-120">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="aed1c-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aed1c-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="aed1c-121">-PublicAccess</span></span>
<span data-ttu-id="aed1c-122">Tároló PublicAccess</span><span class="sxs-lookup"><span data-stu-id="aed1c-122">Container PublicAccess</span></span>

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed1c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aed1c-123">-ResourceGroupName</span></span>
<span data-ttu-id="aed1c-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="aed1c-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="aed1c-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="aed1c-125">-StorageAccount</span></span>
<span data-ttu-id="aed1c-126">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="aed1c-126">Storage account object</span></span>

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

### <span data-ttu-id="aed1c-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aed1c-127">-StorageAccountName</span></span>
<span data-ttu-id="aed1c-128">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="aed1c-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="aed1c-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aed1c-129">-Confirm</span></span>
<span data-ttu-id="aed1c-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aed1c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aed1c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aed1c-131">-WhatIf</span></span>
<span data-ttu-id="aed1c-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aed1c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aed1c-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aed1c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aed1c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed1c-134">CommonParameters</span></span>
<span data-ttu-id="aed1c-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aed1c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed1c-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aed1c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed1c-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aed1c-137">INPUTS</span></span>

### <span data-ttu-id="aed1c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="aed1c-138">System.String</span></span>

## <span data-ttu-id="aed1c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aed1c-139">OUTPUTS</span></span>

### <span data-ttu-id="aed1c-140">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="aed1c-140">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="aed1c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aed1c-141">NOTES</span></span>

## <span data-ttu-id="aed1c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aed1c-142">RELATED LINKS</span></span>

