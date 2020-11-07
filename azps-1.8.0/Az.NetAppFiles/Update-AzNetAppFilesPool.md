---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 3dd02a2dc0cf7090ba2711b6155d25038397ab9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670759"
---
# <span data-ttu-id="009a3-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="009a3-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="009a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="009a3-102">SYNOPSIS</span></span>
<span data-ttu-id="009a3-103">Azure NetApp-fájlok (ANF) készletének frissítése az új adathalmazsal.</span><span class="sxs-lookup"><span data-stu-id="009a3-103">Updates an Azure NetApp Files (ANF) pool with the new data set.</span></span>

## <span data-ttu-id="009a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="009a3-104">SYNTAX</span></span>

### <span data-ttu-id="009a3-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="009a3-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="009a3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="009a3-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String>
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="009a3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="009a3-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -PoolSize <Int64> -ServiceLevel <String> -InputObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="009a3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="009a3-108">DESCRIPTION</span></span>
<span data-ttu-id="009a3-109">Az **Update-AzNetAppFilesPool** parancsmag módosította a ANF-készletet.</span><span class="sxs-lookup"><span data-stu-id="009a3-109">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="009a3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="009a3-110">EXAMPLES</span></span>

### <span data-ttu-id="009a3-111">Példa 1: ANF-készlet módosítása</span><span class="sxs-lookup"><span data-stu-id="009a3-111">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="009a3-112">Ez a parancs a "MyAnfPool" ANF-alkalmazáskészletet a megadott méret és ServiceLevel értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="009a3-112">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="009a3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="009a3-113">PARAMETERS</span></span>

### <span data-ttu-id="009a3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="009a3-114">-AccountName</span></span>
<span data-ttu-id="009a3-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="009a3-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="009a3-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="009a3-116">-AccountObject</span></span>
<span data-ttu-id="009a3-117">A frissítendő készletet tartalmazó ügyfél-objektum</span><span class="sxs-lookup"><span data-stu-id="009a3-117">The account object containing the pool to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="009a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="009a3-118">-DefaultProfile</span></span>
<span data-ttu-id="009a3-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="009a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="009a3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="009a3-120">-InputObject</span></span>
<span data-ttu-id="009a3-121">A frissítendő Pool objektum</span><span class="sxs-lookup"><span data-stu-id="009a3-121">The pool object to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="009a3-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="009a3-122">-Location</span></span>
<span data-ttu-id="009a3-123">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="009a3-123">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="009a3-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="009a3-124">-Name</span></span>
<span data-ttu-id="009a3-125">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="009a3-125">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="009a3-126">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="009a3-126">-PoolSize</span></span>
<span data-ttu-id="009a3-127">A ANF-medence mérete</span><span class="sxs-lookup"><span data-stu-id="009a3-127">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="009a3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="009a3-128">-ResourceGroupName</span></span>
<span data-ttu-id="009a3-129">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="009a3-129">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="009a3-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="009a3-130">-ServiceLevel</span></span>
<span data-ttu-id="009a3-131">A ANF-készlet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="009a3-131">The service level of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="009a3-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="009a3-132">-Confirm</span></span>
<span data-ttu-id="009a3-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="009a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="009a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="009a3-134">-WhatIf</span></span>
<span data-ttu-id="009a3-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="009a3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="009a3-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="009a3-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="009a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="009a3-137">CommonParameters</span></span>
<span data-ttu-id="009a3-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="009a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="009a3-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="009a3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="009a3-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="009a3-140">INPUTS</span></span>

### <span data-ttu-id="009a3-141">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="009a3-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="009a3-142">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="009a3-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="009a3-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="009a3-143">OUTPUTS</span></span>

### <span data-ttu-id="009a3-144">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="009a3-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="009a3-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="009a3-145">NOTES</span></span>

## <span data-ttu-id="009a3-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="009a3-146">RELATED LINKS</span></span>
