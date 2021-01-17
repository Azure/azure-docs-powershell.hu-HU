---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 901061390c68853832bad14965620abad21817e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467954"
---
# <span data-ttu-id="22a59-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="22a59-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="22a59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22a59-102">SYNOPSIS</span></span>
<span data-ttu-id="22a59-103">Tároló blobtárolót hoz létre</span><span class="sxs-lookup"><span data-stu-id="22a59-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="22a59-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22a59-104">SYNTAX</span></span>

### <span data-ttu-id="22a59-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22a59-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22a59-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="22a59-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22a59-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="22a59-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22a59-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="22a59-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22a59-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22a59-109">DESCRIPTION</span></span>
<span data-ttu-id="22a59-110">A **New-AzRmStorageContainer** parancsmag létrehoz egy tároló blobtárolót</span><span class="sxs-lookup"><span data-stu-id="22a59-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="22a59-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22a59-111">EXAMPLES</span></span>

### <span data-ttu-id="22a59-112">1. példa: Tárterület blobtárolójának létrehozása a tárfiók nevével és a tároló nevével metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="22a59-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="22a59-113">Ez a parancs létrehoz egy tároló blobtárolót, amely a tárfiók nevét és a tároló nevét metaadatokkal együtt tárolja.</span><span class="sxs-lookup"><span data-stu-id="22a59-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="22a59-114">2. példa: Tárterület blobtároló létrehozása Tárfiók-objektummal és tárolónévvel, nyilvános hozzáféréssel blobként</span><span class="sxs-lookup"><span data-stu-id="22a59-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="22a59-115">Ez a parancs létrehoz egy Tároló blobtárolót a Tárfiók-objektummal és a tároló nevével, és nyilvános hozzáféréssel blobként.</span><span class="sxs-lookup"><span data-stu-id="22a59-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="22a59-116">3. példa: Tároló létrehozása a EncryptionScope beállítással</span><span class="sxs-lookup"><span data-stu-id="22a59-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
```
PS C:\> $c = New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name testcontainer -DefaultEncryptionScope "testscope" -PreventEncryptionScopeOverride $true

PS C:\> $c

   ResourceGroupName: myResourceGroup, StorageAccountName: myStorageAccount

Name          PublicAccess LastModified HasLegalHold HasImmutabilityPolicy
----          ------------ ------------ ------------ ---------------------
testcontainer                           False        False                

PS C:\> $c.DefaultEncryptionScope
testscope

PS C:\> $c.DenyEncryptionScopeOverride
True
```

<span data-ttu-id="22a59-117">Ez a parancs létrehoz egy defalt encryptionScope értékeket tartalmazó tárolót, és letiltja a titkosítási hatókör felülírást az alapértelmezett tárolóból.</span><span class="sxs-lookup"><span data-stu-id="22a59-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="22a59-118">Ezután mutassa a kapcsolódó tárolótulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="22a59-118">Then show the related container properties.</span></span>

## <span data-ttu-id="22a59-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22a59-119">PARAMETERS</span></span>

### <span data-ttu-id="22a59-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="22a59-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="22a59-121">Alapértelmezés szerint a tároló a megadott titkosítási hatókört használja az összes íráshoz.</span><span class="sxs-lookup"><span data-stu-id="22a59-121">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a59-122">-DefaultProfile</span></span>
<span data-ttu-id="22a59-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22a59-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22a59-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="22a59-124">-Metadata</span></span>
<span data-ttu-id="22a59-125">Tároló metaadatai</span><span class="sxs-lookup"><span data-stu-id="22a59-125">Container Metadata</span></span>

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

### <span data-ttu-id="22a59-126">-Name</span><span class="sxs-lookup"><span data-stu-id="22a59-126">-Name</span></span>
<span data-ttu-id="22a59-127">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="22a59-127">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22a59-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="22a59-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="22a59-129">Tiltsa le a titkosítási hatókör felülírást az alapértelmezett tárolóból.</span><span class="sxs-lookup"><span data-stu-id="22a59-129">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a59-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="22a59-130">-PublicAccess</span></span>
<span data-ttu-id="22a59-131">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="22a59-131">Container PublicAccess</span></span>

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

### <span data-ttu-id="22a59-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a59-132">-ResourceGroupName</span></span>
<span data-ttu-id="22a59-133">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="22a59-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a59-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="22a59-134">-StorageAccount</span></span>
<span data-ttu-id="22a59-135">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="22a59-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22a59-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="22a59-136">-StorageAccountName</span></span>
<span data-ttu-id="22a59-137">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="22a59-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22a59-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22a59-138">-Confirm</span></span>
<span data-ttu-id="22a59-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22a59-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22a59-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22a59-140">-WhatIf</span></span>
<span data-ttu-id="22a59-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22a59-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22a59-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22a59-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22a59-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a59-143">CommonParameters</span></span>
<span data-ttu-id="22a59-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22a59-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a59-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22a59-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a59-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22a59-146">INPUTS</span></span>

### <span data-ttu-id="22a59-147">System.String</span><span class="sxs-lookup"><span data-stu-id="22a59-147">System.String</span></span>

### <span data-ttu-id="22a59-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="22a59-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="22a59-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22a59-149">OUTPUTS</span></span>

### <span data-ttu-id="22a59-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="22a59-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="22a59-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22a59-151">NOTES</span></span>

## <span data-ttu-id="22a59-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22a59-152">RELATED LINKS</span></span>
