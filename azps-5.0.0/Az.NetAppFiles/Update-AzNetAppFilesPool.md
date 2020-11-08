---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: e63812f1972effd7956911861e5c6e07436fd4c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195095"
---
# <span data-ttu-id="b6ed2-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b6ed2-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="b6ed2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ed2-103">Az Azure NetApp-fájlok (ANF) készletének frissítése a megadható feltételes módosítóval összhangban.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="b6ed2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6ed2-104">SYNTAX</span></span>

### <span data-ttu-id="b6ed2-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6ed2-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6ed2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6ed2-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6ed2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6ed2-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6ed2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6ed2-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6ed2-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6ed2-109">DESCRIPTION</span></span>
<span data-ttu-id="b6ed2-110">Az **Update-AzNetAppFilesPool** parancsmag módosította a ANF-készletet.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="b6ed2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b6ed2-111">EXAMPLES</span></span>

### <span data-ttu-id="b6ed2-112">Példa 1: ANF-készlet módosítása</span><span class="sxs-lookup"><span data-stu-id="b6ed2-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -ServiceLevel "Standard"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
ProvisioningState : Succeeded
```

<span data-ttu-id="b6ed2-113">Ez a parancs a "MyAnfPool" ANF-alkalmazáskészletet a megadott méret és ServiceLevel értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="b6ed2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6ed2-114">PARAMETERS</span></span>

### <span data-ttu-id="b6ed2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6ed2-115">-AccountName</span></span>
<span data-ttu-id="b6ed2-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="b6ed2-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="b6ed2-117">-AccountObject</span></span>
<span data-ttu-id="b6ed2-118">A frissítendő készletet tartalmazó ügyfél-objektum</span><span class="sxs-lookup"><span data-stu-id="b6ed2-118">The account object containing the pool to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ed2-119">-DefaultProfile</span></span>
<span data-ttu-id="b6ed2-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6ed2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6ed2-121">-InputObject</span></span>
<span data-ttu-id="b6ed2-122">A frissítendő Pool objektum</span><span class="sxs-lookup"><span data-stu-id="b6ed2-122">The pool object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="b6ed2-123">-Location</span></span>
<span data-ttu-id="b6ed2-124">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="b6ed2-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6ed2-125">-Name</span></span>
<span data-ttu-id="b6ed2-126">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="b6ed2-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="b6ed2-127">-PoolSize</span></span>
<span data-ttu-id="b6ed2-128">A ANF-medence mérete</span><span class="sxs-lookup"><span data-stu-id="b6ed2-128">The size of the ANF pool</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ed2-129">-ResourceGroupName</span></span>
<span data-ttu-id="b6ed2-130">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="b6ed2-130">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6ed2-131">-ResourceId</span></span>
<span data-ttu-id="b6ed2-132">A ANF-készlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b6ed2-132">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="b6ed2-133">-ServiceLevel</span></span>
<span data-ttu-id="b6ed2-134">A ANF-készlet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="b6ed2-134">The service level of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="b6ed2-135">-Tag</span></span>
<span data-ttu-id="b6ed2-136">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="b6ed2-136">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ed2-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6ed2-137">-Confirm</span></span>
<span data-ttu-id="b6ed2-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6ed2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6ed2-139">-WhatIf</span></span>
<span data-ttu-id="b6ed2-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6ed2-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6ed2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ed2-142">CommonParameters</span></span>
<span data-ttu-id="b6ed2-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6ed2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ed2-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b6ed2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ed2-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6ed2-145">INPUTS</span></span>

### <span data-ttu-id="b6ed2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b6ed2-146">System.String</span></span>

### <span data-ttu-id="b6ed2-147">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b6ed2-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="b6ed2-148">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b6ed2-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="b6ed2-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6ed2-149">OUTPUTS</span></span>

### <span data-ttu-id="b6ed2-150">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b6ed2-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="b6ed2-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6ed2-151">NOTES</span></span>

## <span data-ttu-id="b6ed2-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6ed2-152">RELATED LINKS</span></span>
