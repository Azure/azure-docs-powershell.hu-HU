---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185804"
---
# <span data-ttu-id="7ef28-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="7ef28-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="7ef28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ef28-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef28-103">Eltávolítja a meghatározott objektum replikációs házirendjét egy tároló fiókból.</span><span class="sxs-lookup"><span data-stu-id="7ef28-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="7ef28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ef28-104">SYNTAX</span></span>

### <span data-ttu-id="7ef28-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ef28-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ef28-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="7ef28-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ef28-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="7ef28-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ef28-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ef28-108">DESCRIPTION</span></span>
<span data-ttu-id="7ef28-109">A **Remove-AzStorageObjectReplicationPolicy** parancsmag eltávolítja a megadott objektum replikációs házirendjét egy tároló fiókból.</span><span class="sxs-lookup"><span data-stu-id="7ef28-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="7ef28-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7ef28-110">EXAMPLES</span></span>

### <span data-ttu-id="7ef28-111">Példa 1: az objektum replikációs házirendjének eltávolítása bizonyos policyId.</span><span class="sxs-lookup"><span data-stu-id="7ef28-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="7ef28-112">Ez a parancs eltávolítja az objektum replikációs házirendjét a tárolási fiók adott policyId.</span><span class="sxs-lookup"><span data-stu-id="7ef28-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="7ef28-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ef28-113">PARAMETERS</span></span>

### <span data-ttu-id="7ef28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef28-114">-DefaultProfile</span></span>
<span data-ttu-id="7ef28-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ef28-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ef28-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ef28-116">-InputObject</span></span>
<span data-ttu-id="7ef28-117">Objektum-replikációs házirend-objektum törölni.</span><span class="sxs-lookup"><span data-stu-id="7ef28-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="7ef28-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ef28-118">-PassThru</span></span>
<span data-ttu-id="7ef28-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7ef28-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7ef28-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="7ef28-120">-PolicyId</span></span>
<span data-ttu-id="7ef28-121">Az objektum replikációs házirend-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7ef28-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="7ef28-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ef28-122">-ResourceGroupName</span></span>
<span data-ttu-id="7ef28-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7ef28-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="7ef28-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ef28-124">-StorageAccount</span></span>
<span data-ttu-id="7ef28-125">Storage Account objektum</span><span class="sxs-lookup"><span data-stu-id="7ef28-125">Storage account object</span></span>

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

### <span data-ttu-id="7ef28-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7ef28-126">-StorageAccountName</span></span>
<span data-ttu-id="7ef28-127">Tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="7ef28-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="7ef28-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7ef28-128">-Confirm</span></span>
<span data-ttu-id="7ef28-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ef28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ef28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ef28-130">-WhatIf</span></span>
<span data-ttu-id="7ef28-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7ef28-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ef28-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ef28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ef28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef28-133">CommonParameters</span></span>
<span data-ttu-id="7ef28-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ef28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef28-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ef28-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef28-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ef28-136">INPUTS</span></span>

### <span data-ttu-id="7ef28-137">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ef28-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="7ef28-138">Microsoft. Azure. Command. Management. Storage. models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="7ef28-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="7ef28-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ef28-139">OUTPUTS</span></span>

### <span data-ttu-id="7ef28-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ef28-140">System.Boolean</span></span>

## <span data-ttu-id="7ef28-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ef28-141">NOTES</span></span>

## <span data-ttu-id="7ef28-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ef28-142">RELATED LINKS</span></span>