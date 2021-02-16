---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: e1ebab6e0b32c6358defee30512185868581b6e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152067"
---
# <span data-ttu-id="939ad-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="939ad-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="939ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="939ad-102">SYNOPSIS</span></span>
<span data-ttu-id="939ad-103">Létrehoz egy új Azure NetApp-fájlok (ANF) készletet.</span><span class="sxs-lookup"><span data-stu-id="939ad-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="939ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="939ad-104">SYNTAX</span></span>

### <span data-ttu-id="939ad-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="939ad-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="939ad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="939ad-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="939ad-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="939ad-107">DESCRIPTION</span></span>
<span data-ttu-id="939ad-108">A **New-AzNetAppFilesPool** parancsmag ANF-készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="939ad-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="939ad-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="939ad-109">EXAMPLES</span></span>

### <span data-ttu-id="939ad-110">1. példa: ANF-készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="939ad-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium" -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="939ad-111">Ez a parancs létrehozza az új ANF-készletet "MyAnfPool" a "MyAnfAccount" fiókon belül.</span><span class="sxs-lookup"><span data-stu-id="939ad-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="939ad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="939ad-112">PARAMETERS</span></span>

### <span data-ttu-id="939ad-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="939ad-113">-AccountName</span></span>
<span data-ttu-id="939ad-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="939ad-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="939ad-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="939ad-115">-AccountObject</span></span>
<span data-ttu-id="939ad-116">Az új készletobjektum fiókja</span><span class="sxs-lookup"><span data-stu-id="939ad-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="939ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="939ad-117">-DefaultProfile</span></span>
<span data-ttu-id="939ad-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="939ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="939ad-119">-Location</span><span class="sxs-lookup"><span data-stu-id="939ad-119">-Location</span></span>
<span data-ttu-id="939ad-120">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="939ad-120">The location of the resource</span></span>

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

### <span data-ttu-id="939ad-121">-Name</span><span class="sxs-lookup"><span data-stu-id="939ad-121">-Name</span></span>
<span data-ttu-id="939ad-122">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="939ad-122">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="939ad-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="939ad-123">-PoolSize</span></span>
<span data-ttu-id="939ad-124">Az ANF-készlet mérete</span><span class="sxs-lookup"><span data-stu-id="939ad-124">The size of the ANF pool</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="939ad-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="939ad-125">-QosType</span></span>
<span data-ttu-id="939ad-126">A készlet qos típusa.</span><span class="sxs-lookup"><span data-stu-id="939ad-126">The qos type of the pool.</span></span> <span data-ttu-id="939ad-127">Lehetséges értékek: "Automatikus", "Kézi"</span><span class="sxs-lookup"><span data-stu-id="939ad-127">Possible values include: 'Auto', 'Manual'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Auto
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="939ad-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="939ad-128">-ResourceGroupName</span></span>
<span data-ttu-id="939ad-129">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="939ad-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="939ad-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="939ad-130">-ServiceLevel</span></span>
<span data-ttu-id="939ad-131">Az ANF-készlet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="939ad-131">The service level of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="939ad-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="939ad-132">-Tag</span></span>
<span data-ttu-id="939ad-133">Erőforráscímkéket képviselő hashtable</span><span class="sxs-lookup"><span data-stu-id="939ad-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="939ad-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="939ad-134">-Confirm</span></span>
<span data-ttu-id="939ad-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="939ad-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="939ad-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="939ad-136">-WhatIf</span></span>
<span data-ttu-id="939ad-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="939ad-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="939ad-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="939ad-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="939ad-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="939ad-139">CommonParameters</span></span>
<span data-ttu-id="939ad-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="939ad-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="939ad-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="939ad-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="939ad-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="939ad-142">INPUTS</span></span>

### <span data-ttu-id="939ad-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="939ad-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="939ad-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="939ad-144">OUTPUTS</span></span>

### <span data-ttu-id="939ad-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="939ad-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="939ad-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="939ad-146">NOTES</span></span>

## <span data-ttu-id="939ad-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="939ad-147">RELATED LINKS</span></span>
