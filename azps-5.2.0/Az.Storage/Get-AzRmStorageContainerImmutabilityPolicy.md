---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349733"
---
# <span data-ttu-id="19c57-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="19c57-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="19c57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19c57-102">SYNOPSIS</span></span>
<span data-ttu-id="19c57-103">ImmutabilityPolicy of a Storage blob containers</span><span class="sxs-lookup"><span data-stu-id="19c57-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="19c57-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19c57-104">SYNTAX</span></span>

### <span data-ttu-id="19c57-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="19c57-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c57-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="19c57-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c57-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="19c57-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19c57-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19c57-108">DESCRIPTION</span></span>
<span data-ttu-id="19c57-109">A **Get-AzRmStorageContainerImmutabilityPolicy parancsmag** ImmutabilityPolicy típusú blobtárolókat kap</span><span class="sxs-lookup"><span data-stu-id="19c57-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="19c57-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19c57-110">EXAMPLES</span></span>

### <span data-ttu-id="19c57-111">1. példa: A Tárfiók nevét és tárolónevét tartalmazó Tár blobtároló ImmutabilityPolicy-ának lekérte</span><span class="sxs-lookup"><span data-stu-id="19c57-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="19c57-112">Ez a parancs immutabilityPolicy-t kap egy Tároló blobtárolóból, a Tárfiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="19c57-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="19c57-113">2. példa: Tárfiók-objektummal és tárolónévvel egy tároló blobtárolója ImmutabilityPolicy-ának lekérte</span><span class="sxs-lookup"><span data-stu-id="19c57-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="19c57-114">Ez a parancs immutabilityPolicy-t kap egy Tárfiók-objektummal és tárolónévvel.</span><span class="sxs-lookup"><span data-stu-id="19c57-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="19c57-115">3. példa: A Tártároló objektummal tárolt blobtároló ImmutabilityPolicy-ának lekérte</span><span class="sxs-lookup"><span data-stu-id="19c57-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="19c57-116">Ez a parancs immutabilityPolicy-t kap egy Tárolótároló objektummal együtt tároló blobtárolóból.</span><span class="sxs-lookup"><span data-stu-id="19c57-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="19c57-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19c57-117">PARAMETERS</span></span>

### <span data-ttu-id="19c57-118">-Container</span><span class="sxs-lookup"><span data-stu-id="19c57-118">-Container</span></span>
<span data-ttu-id="19c57-119">Tárolóobjektum</span><span class="sxs-lookup"><span data-stu-id="19c57-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19c57-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="19c57-120">-ContainerName</span></span>
<span data-ttu-id="19c57-121">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="19c57-121">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19c57-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c57-122">-DefaultProfile</span></span>
<span data-ttu-id="19c57-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19c57-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19c57-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="19c57-124">-Etag</span></span>
<span data-ttu-id="19c57-125">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="19c57-125">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c57-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c57-126">-ResourceGroupName</span></span>
<span data-ttu-id="19c57-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="19c57-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="19c57-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="19c57-128">-StorageAccount</span></span>
<span data-ttu-id="19c57-129">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="19c57-129">Storage account object</span></span>

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

### <span data-ttu-id="19c57-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="19c57-130">-StorageAccountName</span></span>
<span data-ttu-id="19c57-131">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="19c57-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="19c57-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c57-132">CommonParameters</span></span>
<span data-ttu-id="19c57-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c57-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c57-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c57-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c57-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19c57-135">INPUTS</span></span>

### <span data-ttu-id="19c57-136">System.String</span><span class="sxs-lookup"><span data-stu-id="19c57-136">System.String</span></span>

### <span data-ttu-id="19c57-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19c57-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="19c57-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="19c57-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="19c57-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19c57-139">OUTPUTS</span></span>

### <span data-ttu-id="19c57-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="19c57-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="19c57-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19c57-141">NOTES</span></span>

## <span data-ttu-id="19c57-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19c57-142">RELATED LINKS</span></span>
