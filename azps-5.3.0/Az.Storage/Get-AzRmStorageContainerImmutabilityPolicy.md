---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376276"
---
# <span data-ttu-id="dbddc-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="dbddc-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="dbddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbddc-102">SYNOPSIS</span></span>
<span data-ttu-id="dbddc-103">ImmutabilityPolicy of a Storage blob containers</span><span class="sxs-lookup"><span data-stu-id="dbddc-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="dbddc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dbddc-104">SYNTAX</span></span>

### <span data-ttu-id="dbddc-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dbddc-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbddc-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="dbddc-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbddc-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="dbddc-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbddc-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dbddc-108">DESCRIPTION</span></span>
<span data-ttu-id="dbddc-109">A **Get-AzRmStorageContainerImmutabilityPolicy parancsmag** ImmutabilityPolicy típusú blobtárolókat kap</span><span class="sxs-lookup"><span data-stu-id="dbddc-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="dbddc-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dbddc-110">EXAMPLES</span></span>

### <span data-ttu-id="dbddc-111">1. példa: A Tárfiók nevét és tárolónevét tartalmazó Tár blobtároló ImmutabilityPolicy-ának lekérte</span><span class="sxs-lookup"><span data-stu-id="dbddc-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="dbddc-112">Ez a parancs immutabilityPolicy-t kap egy Tároló blobtárolóból, a Tárfiók nevével és a tároló nevével.</span><span class="sxs-lookup"><span data-stu-id="dbddc-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="dbddc-113">2. példa: Tárfiók-objektummal és tárolónévvel egy tároló blobtárolója ImmutabilityPolicy-ának lekérte</span><span class="sxs-lookup"><span data-stu-id="dbddc-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="dbddc-114">Ez a parancs immutabilityPolicy-t kap egy Tárfiók-objektummal és tárolónévvel.</span><span class="sxs-lookup"><span data-stu-id="dbddc-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="dbddc-115">3. példa: A Tártároló objektummal tárolt blobtároló ImmutabilityPolicy-ának lekérte</span><span class="sxs-lookup"><span data-stu-id="dbddc-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="dbddc-116">Ez a parancs immutabilityPolicy-t kap egy Tárolótároló objektumot tartalmazó Tár blobtárolóból.</span><span class="sxs-lookup"><span data-stu-id="dbddc-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="dbddc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbddc-117">PARAMETERS</span></span>

### <span data-ttu-id="dbddc-118">-Container</span><span class="sxs-lookup"><span data-stu-id="dbddc-118">-Container</span></span>
<span data-ttu-id="dbddc-119">Tárolóobjektum</span><span class="sxs-lookup"><span data-stu-id="dbddc-119">Storage container object</span></span>

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

### <span data-ttu-id="dbddc-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dbddc-120">-ContainerName</span></span>
<span data-ttu-id="dbddc-121">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="dbddc-121">Container Name</span></span>

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

### <span data-ttu-id="dbddc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbddc-122">-DefaultProfile</span></span>
<span data-ttu-id="dbddc-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dbddc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbddc-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="dbddc-124">-Etag</span></span>
<span data-ttu-id="dbddc-125">Immutability policy etag.</span><span class="sxs-lookup"><span data-stu-id="dbddc-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="dbddc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbddc-126">-ResourceGroupName</span></span>
<span data-ttu-id="dbddc-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dbddc-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="dbddc-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="dbddc-128">-StorageAccount</span></span>
<span data-ttu-id="dbddc-129">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="dbddc-129">Storage account object</span></span>

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

### <span data-ttu-id="dbddc-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dbddc-130">-StorageAccountName</span></span>
<span data-ttu-id="dbddc-131">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="dbddc-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="dbddc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbddc-132">CommonParameters</span></span>
<span data-ttu-id="dbddc-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbddc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbddc-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbddc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbddc-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbddc-135">INPUTS</span></span>

### <span data-ttu-id="dbddc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="dbddc-136">System.String</span></span>

### <span data-ttu-id="dbddc-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dbddc-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="dbddc-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="dbddc-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="dbddc-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbddc-139">OUTPUTS</span></span>

### <span data-ttu-id="dbddc-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="dbddc-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="dbddc-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dbddc-141">NOTES</span></span>

## <span data-ttu-id="dbddc-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbddc-142">RELATED LINKS</span></span>
