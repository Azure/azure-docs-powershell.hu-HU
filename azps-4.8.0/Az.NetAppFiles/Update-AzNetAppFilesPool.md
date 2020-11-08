---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: e63812f1972effd7956911861e5c6e07436fd4c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025245"
---
# <span data-ttu-id="e77dc-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e77dc-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="e77dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e77dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e77dc-103">Az Azure NetApp-fájlok (ANF) készletének frissítése a megadható feltételes módosítóval összhangban.</span><span class="sxs-lookup"><span data-stu-id="e77dc-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="e77dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e77dc-104">SYNTAX</span></span>

### <span data-ttu-id="e77dc-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e77dc-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e77dc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e77dc-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e77dc-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e77dc-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e77dc-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e77dc-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e77dc-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e77dc-109">DESCRIPTION</span></span>
<span data-ttu-id="e77dc-110">Az **Update-AzNetAppFilesPool** parancsmag módosította a ANF-készletet.</span><span class="sxs-lookup"><span data-stu-id="e77dc-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="e77dc-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e77dc-111">EXAMPLES</span></span>

### <span data-ttu-id="e77dc-112">Példa 1: ANF-készlet módosítása</span><span class="sxs-lookup"><span data-stu-id="e77dc-112">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="e77dc-113">Ez a parancs a "MyAnfPool" ANF-alkalmazáskészletet a megadott méret és ServiceLevel értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="e77dc-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="e77dc-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e77dc-114">PARAMETERS</span></span>

### <span data-ttu-id="e77dc-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e77dc-115">-AccountName</span></span>
<span data-ttu-id="e77dc-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="e77dc-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="e77dc-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="e77dc-117">-AccountObject</span></span>
<span data-ttu-id="e77dc-118">A frissítendő készletet tartalmazó ügyfél-objektum</span><span class="sxs-lookup"><span data-stu-id="e77dc-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="e77dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e77dc-119">-DefaultProfile</span></span>
<span data-ttu-id="e77dc-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e77dc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e77dc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e77dc-121">-InputObject</span></span>
<span data-ttu-id="e77dc-122">A frissítendő Pool objektum</span><span class="sxs-lookup"><span data-stu-id="e77dc-122">The pool object to update</span></span>

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

### <span data-ttu-id="e77dc-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="e77dc-123">-Location</span></span>
<span data-ttu-id="e77dc-124">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="e77dc-124">The location of the resource</span></span>

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

### <span data-ttu-id="e77dc-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e77dc-125">-Name</span></span>
<span data-ttu-id="e77dc-126">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="e77dc-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="e77dc-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="e77dc-127">-PoolSize</span></span>
<span data-ttu-id="e77dc-128">A ANF-medence mérete</span><span class="sxs-lookup"><span data-stu-id="e77dc-128">The size of the ANF pool</span></span>

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

### <span data-ttu-id="e77dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e77dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="e77dc-130">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="e77dc-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="e77dc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e77dc-131">-ResourceId</span></span>
<span data-ttu-id="e77dc-132">A ANF-készlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e77dc-132">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="e77dc-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="e77dc-133">-ServiceLevel</span></span>
<span data-ttu-id="e77dc-134">A ANF-készlet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="e77dc-134">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="e77dc-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="e77dc-135">-Tag</span></span>
<span data-ttu-id="e77dc-136">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="e77dc-136">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="e77dc-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e77dc-137">-Confirm</span></span>
<span data-ttu-id="e77dc-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e77dc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e77dc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e77dc-139">-WhatIf</span></span>
<span data-ttu-id="e77dc-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e77dc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e77dc-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e77dc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e77dc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e77dc-142">CommonParameters</span></span>
<span data-ttu-id="e77dc-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e77dc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e77dc-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e77dc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e77dc-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e77dc-145">INPUTS</span></span>

### <span data-ttu-id="e77dc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e77dc-146">System.String</span></span>

### <span data-ttu-id="e77dc-147">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e77dc-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="e77dc-148">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e77dc-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="e77dc-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e77dc-149">OUTPUTS</span></span>

### <span data-ttu-id="e77dc-150">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e77dc-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="e77dc-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e77dc-151">NOTES</span></span>

## <span data-ttu-id="e77dc-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e77dc-152">RELATED LINKS</span></span>
