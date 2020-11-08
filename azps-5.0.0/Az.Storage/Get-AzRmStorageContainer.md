---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: da0ccdc791318f0a315bea8d2464d8d0852aec8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195477"
---
# <span data-ttu-id="6be70-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6be70-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="6be70-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6be70-102">SYNOPSIS</span></span>
<span data-ttu-id="6be70-103">Tároló blob-tárolók beolvasása vagy listázása</span><span class="sxs-lookup"><span data-stu-id="6be70-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="6be70-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6be70-104">SYNTAX</span></span>

### <span data-ttu-id="6be70-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6be70-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6be70-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6be70-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6be70-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6be70-107">DESCRIPTION</span></span>
<span data-ttu-id="6be70-108">A **Get-AzRmStorageContainer** parancsmag tároló blob-tárolókat kap vagy listáz</span><span class="sxs-lookup"><span data-stu-id="6be70-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="6be70-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6be70-109">EXAMPLES</span></span>

### <span data-ttu-id="6be70-110">Példa 1: tároló blob-tároló beszerzése tárolási fiók nevével és a tároló nevével</span><span class="sxs-lookup"><span data-stu-id="6be70-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="6be70-111">Ez a parancs a tároló blob-tárolóját a tárolási fiók nevével és a tároló nevével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6be70-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="6be70-112">2. példa: a tárolási fiók minden tároló blob-tárolójának listázása</span><span class="sxs-lookup"><span data-stu-id="6be70-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="6be70-113">Ez a parancs felsorolja az összes tárterület-tároló blob-tárolóját a tárolási fiók nevével.</span><span class="sxs-lookup"><span data-stu-id="6be70-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="6be70-114">3. példa: adattároló blob-tároló beszerzése tárolási fiók objektummal és tároló nevével</span><span class="sxs-lookup"><span data-stu-id="6be70-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="6be70-115">Ez a parancs egy tároló BLOB-tárolót kap a Storage Account objektummal és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="6be70-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="6be70-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6be70-116">PARAMETERS</span></span>

### <span data-ttu-id="6be70-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6be70-117">-AsJob</span></span>
<span data-ttu-id="6be70-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6be70-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6be70-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be70-119">-DefaultProfile</span></span>
<span data-ttu-id="6be70-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6be70-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6be70-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6be70-121">-Name</span></span>
<span data-ttu-id="6be70-122">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="6be70-122">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6be70-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6be70-123">-ResourceGroupName</span></span>
<span data-ttu-id="6be70-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6be70-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be70-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6be70-125">-StorageAccount</span></span>
<span data-ttu-id="6be70-126">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="6be70-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6be70-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6be70-127">-StorageAccountName</span></span>
<span data-ttu-id="6be70-128">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="6be70-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be70-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be70-129">CommonParameters</span></span>
<span data-ttu-id="6be70-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6be70-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be70-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6be70-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be70-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6be70-132">INPUTS</span></span>

### <span data-ttu-id="6be70-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6be70-133">System.String</span></span>

### <span data-ttu-id="6be70-134">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6be70-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="6be70-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6be70-135">OUTPUTS</span></span>

### <span data-ttu-id="6be70-136">Microsoft. Azure. Command. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="6be70-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="6be70-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6be70-137">NOTES</span></span>

## <span data-ttu-id="6be70-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6be70-138">RELATED LINKS</span></span>
