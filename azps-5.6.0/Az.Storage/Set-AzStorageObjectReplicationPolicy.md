---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: e5d141672fe2f620fc86306b79069d309235393f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929690"
---
# <span data-ttu-id="424aa-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="424aa-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="424aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="424aa-102">SYNOPSIS</span></span>
<span data-ttu-id="424aa-103">Létrehozza vagy frissíti a megadott objektumreplikációs házirendet egy tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="424aa-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="424aa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="424aa-104">SYNTAX</span></span>

### <span data-ttu-id="424aa-105">AccountName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="424aa-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="424aa-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="424aa-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="424aa-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="424aa-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="424aa-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="424aa-108">DESCRIPTION</span></span>
<span data-ttu-id="424aa-109">A **Set-AzStorageObjectReplicationPolicy parancsmag** létrehozza vagy frissíti a megadott objektum-replikációs házirendet egy tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="424aa-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="424aa-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="424aa-110">EXAMPLES</span></span>

### <span data-ttu-id="424aa-111">1. példa: Az objektum-replikációs házirend beállítása célhelyre és forrásfiókra is.</span><span class="sxs-lookup"><span data-stu-id="424aa-111">Example 1: Set object replication policy to both destination and source account.</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $destPolicy = Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId default -SourceAccount $srcAccountName  -Rule $rule1,$rule2

PS C:\> $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mysourceaccount" -InputObject $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----                                     
myresourcegroup   mysourceaccount    56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
```

<span data-ttu-id="424aa-112">Ez a parancs az objektum-replikációs házirendet cél- és forrásfiókra egyaránt beállítja.</span><span class="sxs-lookup"><span data-stu-id="424aa-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="424aa-113">Először hozzon létre 2 objektumreplikációs házirendszabályt, és állítsa be a 2 szabályt a célfiókra.</span><span class="sxs-lookup"><span data-stu-id="424aa-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="424aa-114">Ezután állítsa be az objektum-replikációs házirendet célfiókról forrásfiókra.</span><span class="sxs-lookup"><span data-stu-id="424aa-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="424aa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="424aa-115">PARAMETERS</span></span>

### <span data-ttu-id="424aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424aa-116">-DefaultProfile</span></span>
<span data-ttu-id="424aa-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="424aa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="424aa-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="424aa-118">-DestinationAccount</span></span>
<span data-ttu-id="424aa-119">Object Replication Policy DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="424aa-119">Object Replication Policy DestinationAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424aa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="424aa-120">-InputObject</span></span>
<span data-ttu-id="424aa-121">A megadott fiókra beállítható objektum-replikációs házirendobjektum.</span><span class="sxs-lookup"><span data-stu-id="424aa-121">Object Replication Policy Object to Set to the specified Account.</span></span>

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

### <span data-ttu-id="424aa-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="424aa-122">-PolicyId</span></span>
<span data-ttu-id="424aa-123">Objektum-replikációs házirend azonosítója. GuiD vagy "alapértelmezett" azonosítónak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="424aa-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="424aa-124">Ha nem adja meg a PolicyId értéket, az "alapértelmezett" értéket fogja használni, ami azt jelenti, hogy új házirendet hoz létre, és az új házirend azonosítóját adja vissza a létrehozott házirendben.</span><span class="sxs-lookup"><span data-stu-id="424aa-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424aa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424aa-125">-ResourceGroupName</span></span>
<span data-ttu-id="424aa-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="424aa-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424aa-127">-Rule</span><span class="sxs-lookup"><span data-stu-id="424aa-127">-Rule</span></span>
<span data-ttu-id="424aa-128">Objektum-replikációs házirendszabályok.</span><span class="sxs-lookup"><span data-stu-id="424aa-128">Object Replication Policy Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule[]
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424aa-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="424aa-129">-SourceAccount</span></span>
<span data-ttu-id="424aa-130">Object Replication Policy SourceAccount.</span><span class="sxs-lookup"><span data-stu-id="424aa-130">Object Replication Policy SourceAccount.</span></span>

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

### <span data-ttu-id="424aa-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="424aa-131">-StorageAccount</span></span>
<span data-ttu-id="424aa-132">Tárfiók objektum</span><span class="sxs-lookup"><span data-stu-id="424aa-132">Storage account object</span></span>

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

### <span data-ttu-id="424aa-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="424aa-133">-StorageAccountName</span></span>
<span data-ttu-id="424aa-134">Tárfiók neve.</span><span class="sxs-lookup"><span data-stu-id="424aa-134">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424aa-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="424aa-135">-Confirm</span></span>
<span data-ttu-id="424aa-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="424aa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="424aa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="424aa-137">-WhatIf</span></span>
<span data-ttu-id="424aa-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="424aa-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="424aa-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="424aa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="424aa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424aa-140">CommonParameters</span></span>
<span data-ttu-id="424aa-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424aa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424aa-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424aa-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424aa-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="424aa-143">INPUTS</span></span>

### <span data-ttu-id="424aa-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="424aa-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="424aa-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="424aa-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="424aa-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="424aa-146">OUTPUTS</span></span>

### <span data-ttu-id="424aa-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="424aa-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="424aa-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="424aa-148">NOTES</span></span>

## <span data-ttu-id="424aa-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="424aa-149">RELATED LINKS</span></span>
