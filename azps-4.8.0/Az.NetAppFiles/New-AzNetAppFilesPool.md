---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: f3b1a6180fb59b3c44942459e09a22a333fc9720
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025244"
---
# <span data-ttu-id="6402b-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6402b-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="6402b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6402b-102">SYNOPSIS</span></span>
<span data-ttu-id="6402b-103">Új Azure NetApp-fájlokat (ANF) tartalmazó készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6402b-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="6402b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6402b-104">SYNTAX</span></span>

### <span data-ttu-id="6402b-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6402b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6402b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6402b-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6402b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6402b-107">DESCRIPTION</span></span>
<span data-ttu-id="6402b-108">A **New-AzNetAppFilesPool** parancsmag ANF-készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6402b-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="6402b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6402b-109">EXAMPLES</span></span>

### <span data-ttu-id="6402b-110">1. példa: ANF-készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="6402b-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="6402b-111">Ezzel a paranccsal létrejön az új ANF pool "MyAnfPool" a "MyAnfAccount" fiókon belül.</span><span class="sxs-lookup"><span data-stu-id="6402b-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="6402b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6402b-112">PARAMETERS</span></span>

### <span data-ttu-id="6402b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6402b-113">-AccountName</span></span>
<span data-ttu-id="6402b-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="6402b-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="6402b-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6402b-115">-AccountObject</span></span>
<span data-ttu-id="6402b-116">Az új Pool objektum fiókja</span><span class="sxs-lookup"><span data-stu-id="6402b-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="6402b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6402b-117">-DefaultProfile</span></span>
<span data-ttu-id="6402b-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6402b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6402b-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="6402b-119">-Location</span></span>
<span data-ttu-id="6402b-120">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="6402b-120">The location of the resource</span></span>

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

### <span data-ttu-id="6402b-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6402b-121">-Name</span></span>
<span data-ttu-id="6402b-122">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="6402b-122">The name of the ANF pool</span></span>

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

### <span data-ttu-id="6402b-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="6402b-123">-PoolSize</span></span>
<span data-ttu-id="6402b-124">A ANF-medence mérete</span><span class="sxs-lookup"><span data-stu-id="6402b-124">The size of the ANF pool</span></span>

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

### <span data-ttu-id="6402b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6402b-125">-ResourceGroupName</span></span>
<span data-ttu-id="6402b-126">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="6402b-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="6402b-127">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="6402b-127">-ServiceLevel</span></span>
<span data-ttu-id="6402b-128">A ANF-készlet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="6402b-128">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="6402b-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="6402b-129">-Tag</span></span>
<span data-ttu-id="6402b-130">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="6402b-130">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="6402b-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6402b-131">-Confirm</span></span>
<span data-ttu-id="6402b-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6402b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6402b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6402b-133">-WhatIf</span></span>
<span data-ttu-id="6402b-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6402b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6402b-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6402b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6402b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6402b-136">CommonParameters</span></span>
<span data-ttu-id="6402b-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6402b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6402b-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6402b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6402b-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6402b-139">INPUTS</span></span>

### <span data-ttu-id="6402b-140">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6402b-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="6402b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6402b-141">OUTPUTS</span></span>

### <span data-ttu-id="6402b-142">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6402b-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="6402b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6402b-143">NOTES</span></span>

## <span data-ttu-id="6402b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6402b-144">RELATED LINKS</span></span>
