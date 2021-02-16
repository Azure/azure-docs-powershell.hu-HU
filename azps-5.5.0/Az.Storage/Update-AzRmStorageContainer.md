---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157914"
---
# <span data-ttu-id="0182a-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0182a-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="0182a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0182a-102">SYNOPSIS</span></span>
<span data-ttu-id="0182a-103">Tár blobtárolót módosít</span><span class="sxs-lookup"><span data-stu-id="0182a-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="0182a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0182a-104">SYNTAX</span></span>

### <span data-ttu-id="0182a-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0182a-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0182a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0182a-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0182a-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="0182a-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0182a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0182a-108">DESCRIPTION</span></span>
<span data-ttu-id="0182a-109">Az **Update-AzRmStorageContainer** parancsmag módosítja a Tároló blobtárolót</span><span class="sxs-lookup"><span data-stu-id="0182a-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="0182a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0182a-110">EXAMPLES</span></span>

### <span data-ttu-id="0182a-111">1. példa: Egy tároló blobtárolójának metaadatait és nyilvános hozzáférését módosítja tárfióknévvel és tárolónévvel</span><span class="sxs-lookup"><span data-stu-id="0182a-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="0182a-112">Ez a parancs módosítja egy tároló blobtárolójának metaadatait és nyilvános hozzáférését tárfióknévvel és tárolónévvel.</span><span class="sxs-lookup"><span data-stu-id="0182a-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="0182a-113">2. példa: Nyilvános hozzáférés letiltása egy Tárfiók-objektummal és tárolónévvel egy tár blobtárolóban</span><span class="sxs-lookup"><span data-stu-id="0182a-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="0182a-114">Ez a parancs letiltja a nyilvános hozzáférést egy Tárfiók-objektummal és tárolónévvel tartalmazó tár blobtárolóban.</span><span class="sxs-lookup"><span data-stu-id="0182a-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="0182a-115">3. példa: Nyilvános hozzáférés beállítása Blob-ként egy tárfiók összes tár blobtárolója számára folyamatban lévő tárfiókban</span><span class="sxs-lookup"><span data-stu-id="0182a-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="0182a-116">Ezzel a paranccsal blobként állíthatja be a nyilvános hozzáférést egy tárfiók összes tárterület-blobtárolója számára.</span><span class="sxs-lookup"><span data-stu-id="0182a-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="0182a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0182a-117">PARAMETERS</span></span>

### <span data-ttu-id="0182a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0182a-118">-DefaultProfile</span></span>
<span data-ttu-id="0182a-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0182a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0182a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0182a-120">-InputObject</span></span>
<span data-ttu-id="0182a-121">Tárolóobjektum</span><span class="sxs-lookup"><span data-stu-id="0182a-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0182a-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0182a-122">-Metadata</span></span>
<span data-ttu-id="0182a-123">Tároló metaadatai</span><span class="sxs-lookup"><span data-stu-id="0182a-123">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0182a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0182a-124">-Name</span></span>
<span data-ttu-id="0182a-125">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="0182a-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0182a-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="0182a-126">-PublicAccess</span></span>
<span data-ttu-id="0182a-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="0182a-127">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0182a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0182a-128">-ResourceGroupName</span></span>
<span data-ttu-id="0182a-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0182a-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="0182a-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0182a-130">-StorageAccount</span></span>
<span data-ttu-id="0182a-131">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="0182a-131">Storage account object</span></span>

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

### <span data-ttu-id="0182a-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0182a-132">-StorageAccountName</span></span>
<span data-ttu-id="0182a-133">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="0182a-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="0182a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0182a-134">-Confirm</span></span>
<span data-ttu-id="0182a-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0182a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0182a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0182a-136">-WhatIf</span></span>
<span data-ttu-id="0182a-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0182a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0182a-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0182a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0182a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0182a-139">CommonParameters</span></span>
<span data-ttu-id="0182a-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0182a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0182a-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0182a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0182a-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0182a-142">INPUTS</span></span>

### <span data-ttu-id="0182a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0182a-143">System.String</span></span>

### <span data-ttu-id="0182a-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0182a-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0182a-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="0182a-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="0182a-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0182a-146">OUTPUTS</span></span>

### <span data-ttu-id="0182a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="0182a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="0182a-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0182a-148">NOTES</span></span>

## <span data-ttu-id="0182a-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0182a-149">RELATED LINKS</span></span>
