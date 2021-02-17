---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 8f26023224e0f6d4a035f4671db7b45be57a3177
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147187"
---
# <span data-ttu-id="1ffa3-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="1ffa3-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="1ffa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ffa3-102">SYNOPSIS</span></span>
<span data-ttu-id="1ffa3-103">Frissíti az Azure NetApp-fájlokat (ANF)-készletet a megadott opcionális módosítóknak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="1ffa3-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="1ffa3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ffa3-104">SYNTAX</span></span>

### <span data-ttu-id="1ffa3-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ffa3-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ffa3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ffa3-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ffa3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ffa3-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ffa3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ffa3-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ffa3-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ffa3-109">DESCRIPTION</span></span>
<span data-ttu-id="1ffa3-110">Az **Update-AzNetAppFilesPool** parancsmag módosítja az ANF-készletet.</span><span class="sxs-lookup"><span data-stu-id="1ffa3-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="1ffa3-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ffa3-111">EXAMPLES</span></span>

### <span data-ttu-id="1ffa3-112">1. példa: ANF-készlet módosítása</span><span class="sxs-lookup"><span data-stu-id="1ffa3-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="1ffa3-113">Ez a parancs módosítja a "MyAnfPool" ANF készletet a megadott méretűre és QosType-típusra.</span><span class="sxs-lookup"><span data-stu-id="1ffa3-113">This command changes the ANF pool "MyAnfPool" to have the given size and QosType.</span></span>

## <span data-ttu-id="1ffa3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ffa3-114">PARAMETERS</span></span>

### <span data-ttu-id="1ffa3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1ffa3-115">-AccountName</span></span>
<span data-ttu-id="1ffa3-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="1ffa3-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="1ffa3-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="1ffa3-117">-AccountObject</span></span>
<span data-ttu-id="1ffa3-118">A frissítenie kell a készletet tartalmazó fiókobjektum</span><span class="sxs-lookup"><span data-stu-id="1ffa3-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="1ffa3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ffa3-119">-DefaultProfile</span></span>
<span data-ttu-id="1ffa3-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ffa3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ffa3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ffa3-121">-InputObject</span></span>
<span data-ttu-id="1ffa3-122">Frissítend kell a készletobjektumot</span><span class="sxs-lookup"><span data-stu-id="1ffa3-122">The pool object to update</span></span>

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

### <span data-ttu-id="1ffa3-123">-Location</span><span class="sxs-lookup"><span data-stu-id="1ffa3-123">-Location</span></span>
<span data-ttu-id="1ffa3-124">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="1ffa3-124">The location of the resource</span></span>

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

### <span data-ttu-id="1ffa3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1ffa3-125">-Name</span></span>
<span data-ttu-id="1ffa3-126">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="1ffa3-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="1ffa3-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="1ffa3-127">-PoolSize</span></span>
<span data-ttu-id="1ffa3-128">Az ANF-készlet mérete</span><span class="sxs-lookup"><span data-stu-id="1ffa3-128">The size of the ANF pool</span></span>

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

### <span data-ttu-id="1ffa3-129">-QosType</span><span class="sxs-lookup"><span data-stu-id="1ffa3-129">-QosType</span></span>
<span data-ttu-id="1ffa3-130">A készlet qos típusa.</span><span class="sxs-lookup"><span data-stu-id="1ffa3-130">The qos type of the pool.</span></span> <span data-ttu-id="1ffa3-131">Lehetséges értékek: "Automatikus", "Kézi"</span><span class="sxs-lookup"><span data-stu-id="1ffa3-131">Possible values include: 'Auto', 'Manual'</span></span>

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

### <span data-ttu-id="1ffa3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ffa3-132">-ResourceGroupName</span></span>
<span data-ttu-id="1ffa3-133">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="1ffa3-133">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1ffa3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ffa3-134">-ResourceId</span></span>
<span data-ttu-id="1ffa3-135">Az ANF-készlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1ffa3-135">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="1ffa3-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ffa3-136">-Tag</span></span>
<span data-ttu-id="1ffa3-137">Erőforráscímkéket képviselő hashtable</span><span class="sxs-lookup"><span data-stu-id="1ffa3-137">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="1ffa3-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ffa3-138">-Confirm</span></span>
<span data-ttu-id="1ffa3-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1ffa3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ffa3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ffa3-140">-WhatIf</span></span>
<span data-ttu-id="1ffa3-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1ffa3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ffa3-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ffa3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ffa3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ffa3-143">CommonParameters</span></span>
<span data-ttu-id="1ffa3-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ffa3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ffa3-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ffa3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ffa3-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ffa3-146">INPUTS</span></span>

### <span data-ttu-id="1ffa3-147">System.String</span><span class="sxs-lookup"><span data-stu-id="1ffa3-147">System.String</span></span>

### <span data-ttu-id="1ffa3-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1ffa3-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="1ffa3-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="1ffa3-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="1ffa3-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ffa3-150">OUTPUTS</span></span>

### <span data-ttu-id="1ffa3-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="1ffa3-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="1ffa3-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ffa3-152">NOTES</span></span>

## <span data-ttu-id="1ffa3-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ffa3-153">RELATED LINKS</span></span>
