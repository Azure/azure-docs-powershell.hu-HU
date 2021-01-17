---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466905"
---
# <span data-ttu-id="49c28-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="49c28-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="49c28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49c28-102">SYNOPSIS</span></span>
<span data-ttu-id="49c28-103">Eltávolítja a megadott objektumreplikációs házirendet egy tárfiókból.</span><span class="sxs-lookup"><span data-stu-id="49c28-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="49c28-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49c28-104">SYNTAX</span></span>

### <span data-ttu-id="49c28-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49c28-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49c28-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="49c28-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49c28-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="49c28-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49c28-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49c28-108">DESCRIPTION</span></span>
<span data-ttu-id="49c28-109">A **Remove-AzStorageObjectReplicationPolicy parancsmag** eltávolítja a megadott objektum-replikációs házirendet egy tárfiókból.</span><span class="sxs-lookup"><span data-stu-id="49c28-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="49c28-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49c28-110">EXAMPLES</span></span>

### <span data-ttu-id="49c28-111">1. példa: Tárfiókból eltávolíthat egy adott házirendazonosítóval megadott objektumreplikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="49c28-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="49c28-112">Ez a parancs eltávolít egy tárfiókból egy adott házirendazonosítóval megadott objektumreplikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="49c28-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="49c28-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49c28-113">PARAMETERS</span></span>

### <span data-ttu-id="49c28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c28-114">-DefaultProfile</span></span>
<span data-ttu-id="49c28-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49c28-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49c28-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49c28-116">-InputObject</span></span>
<span data-ttu-id="49c28-117">Törlünk egy objektum-replikációs házirendobjektumot.</span><span class="sxs-lookup"><span data-stu-id="49c28-117">Object Replication Policy object to Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49c28-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49c28-118">-PassThru</span></span>
<span data-ttu-id="49c28-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="49c28-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="49c28-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="49c28-120">-PolicyId</span></span>
<span data-ttu-id="49c28-121">Objektum-replikációs házirend azonosítója.</span><span class="sxs-lookup"><span data-stu-id="49c28-121">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c28-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c28-122">-ResourceGroupName</span></span>
<span data-ttu-id="49c28-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="49c28-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="49c28-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="49c28-124">-StorageAccount</span></span>
<span data-ttu-id="49c28-125">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="49c28-125">Storage account object</span></span>

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

### <span data-ttu-id="49c28-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="49c28-126">-StorageAccountName</span></span>
<span data-ttu-id="49c28-127">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="49c28-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c28-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49c28-128">-Confirm</span></span>
<span data-ttu-id="49c28-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="49c28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49c28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49c28-130">-WhatIf</span></span>
<span data-ttu-id="49c28-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="49c28-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49c28-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49c28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49c28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c28-133">CommonParameters</span></span>
<span data-ttu-id="49c28-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c28-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49c28-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c28-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49c28-136">INPUTS</span></span>

### <span data-ttu-id="49c28-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="49c28-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="49c28-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="49c28-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="49c28-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49c28-139">OUTPUTS</span></span>

### <span data-ttu-id="49c28-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49c28-140">System.Boolean</span></span>

## <span data-ttu-id="49c28-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49c28-141">NOTES</span></span>

## <span data-ttu-id="49c28-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49c28-142">RELATED LINKS</span></span>
