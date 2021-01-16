---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 06a37226c1915ef858d72ec123dd238011c19f19
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324879"
---
# <span data-ttu-id="d2ec3-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d2ec3-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="d2ec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ec3-103">Tároló blobtárolót hoz létre</span><span class="sxs-lookup"><span data-stu-id="d2ec3-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="d2ec3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d2ec3-104">SYNTAX</span></span>

### <span data-ttu-id="d2ec3-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2ec3-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ec3-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d2ec3-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ec3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d2ec3-107">DESCRIPTION</span></span>
<span data-ttu-id="d2ec3-108">A **New-AzRmStorageContainer** parancsmag létrehoz egy tároló blobtárolót</span><span class="sxs-lookup"><span data-stu-id="d2ec3-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="d2ec3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d2ec3-109">EXAMPLES</span></span>

### <span data-ttu-id="d2ec3-110">1. példa: Tárterület blobtárolójának létrehozása a tárfiók nevével és a tároló nevével metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="d2ec3-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="d2ec3-111">Ez a parancs létrehoz egy tároló blobtárolót, amely a tárfiók nevét és a tároló nevét metaadatokkal együtt tárolja.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="d2ec3-112">2. példa: Tárterület blobtároló létrehozása Tárfiók-objektummal és tárolónévvel, nyilvános hozzáféréssel blobként</span><span class="sxs-lookup"><span data-stu-id="d2ec3-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="d2ec3-113">Ez a parancs létrehoz egy Tároló blobtárolót a Tárfiók-objektummal és a tároló nevével, nyilvános hozzáféréssel blobként.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="d2ec3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2ec3-114">PARAMETERS</span></span>

### <span data-ttu-id="d2ec3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ec3-115">-DefaultProfile</span></span>
<span data-ttu-id="d2ec3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2ec3-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d2ec3-117">-Metadata</span></span>
<span data-ttu-id="d2ec3-118">Tároló metaadatai</span><span class="sxs-lookup"><span data-stu-id="d2ec3-118">Container Metadata</span></span>

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

### <span data-ttu-id="d2ec3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d2ec3-119">-Name</span></span>
<span data-ttu-id="d2ec3-120">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="d2ec3-120">Container Name</span></span>

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

### <span data-ttu-id="d2ec3-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="d2ec3-121">-PublicAccess</span></span>
<span data-ttu-id="d2ec3-122">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="d2ec3-122">Container PublicAccess</span></span>

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

### <span data-ttu-id="d2ec3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ec3-123">-ResourceGroupName</span></span>
<span data-ttu-id="d2ec3-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="d2ec3-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2ec3-125">-StorageAccount</span></span>
<span data-ttu-id="d2ec3-126">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="d2ec3-126">Storage account object</span></span>

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

### <span data-ttu-id="d2ec3-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d2ec3-127">-StorageAccountName</span></span>
<span data-ttu-id="d2ec3-128">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="d2ec3-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2ec3-129">-Confirm</span></span>
<span data-ttu-id="d2ec3-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2ec3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ec3-131">-WhatIf</span></span>
<span data-ttu-id="d2ec3-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2ec3-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2ec3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ec3-134">CommonParameters</span></span>
<span data-ttu-id="d2ec3-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ec3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ec3-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ec3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ec3-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2ec3-137">INPUTS</span></span>

### <span data-ttu-id="d2ec3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d2ec3-138">System.String</span></span>

### <span data-ttu-id="d2ec3-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2ec3-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d2ec3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2ec3-140">OUTPUTS</span></span>

### <span data-ttu-id="d2ec3-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="d2ec3-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="d2ec3-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d2ec3-142">NOTES</span></span>

## <span data-ttu-id="d2ec3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2ec3-143">RELATED LINKS</span></span>
