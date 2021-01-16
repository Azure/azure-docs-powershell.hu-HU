---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 1a04f128326c0b2259b81d6c58c4bc7b0113e9db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466259"
---
# <span data-ttu-id="86f04-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="86f04-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="86f04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86f04-102">SYNOPSIS</span></span>
<span data-ttu-id="86f04-103">Részleteket kap az Azure NetApp-fájlok (ANF) kötetről.</span><span class="sxs-lookup"><span data-stu-id="86f04-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="86f04-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="86f04-104">SYNTAX</span></span>

### <span data-ttu-id="86f04-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86f04-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86f04-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86f04-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86f04-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86f04-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86f04-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="86f04-108">DESCRIPTION</span></span>
<span data-ttu-id="86f04-109">A **Get-AzNetAppFilesVolume** parancsmag anF-kötetek részleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="86f04-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="86f04-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="86f04-110">EXAMPLES</span></span>

### <span data-ttu-id="86f04-111">1. példa: ANF-hangerő lekérte</span><span class="sxs-lookup"><span data-stu-id="86f04-111">Example 1: Get an ANF volume</span></span>
```
PS C:\>Get-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     :
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="86f04-112">Ez a parancs a MyAnfVolume nevű kötetet a "MyAnfPool" készletből kapja meg.</span><span class="sxs-lookup"><span data-stu-id="86f04-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="86f04-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86f04-113">PARAMETERS</span></span>

### <span data-ttu-id="86f04-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="86f04-114">-AccountName</span></span>
<span data-ttu-id="86f04-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="86f04-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="86f04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f04-116">-DefaultProfile</span></span>
<span data-ttu-id="86f04-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86f04-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86f04-118">-Name</span><span class="sxs-lookup"><span data-stu-id="86f04-118">-Name</span></span>
<span data-ttu-id="86f04-119">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="86f04-119">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f04-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="86f04-120">-PoolName</span></span>
<span data-ttu-id="86f04-121">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="86f04-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="86f04-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="86f04-122">-PoolObject</span></span>
<span data-ttu-id="86f04-123">A vissza nem térhet mennyiséget tartalmazó készletobjektum</span><span class="sxs-lookup"><span data-stu-id="86f04-123">The pool object containing the volume to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86f04-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86f04-124">-ResourceGroupName</span></span>
<span data-ttu-id="86f04-125">Az ANF-mennyiség erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="86f04-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="86f04-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86f04-126">-ResourceId</span></span>
<span data-ttu-id="86f04-127">Az ANF-mennyiség erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="86f04-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="86f04-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f04-128">CommonParameters</span></span>
<span data-ttu-id="86f04-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86f04-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f04-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86f04-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f04-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86f04-131">INPUTS</span></span>

### <span data-ttu-id="86f04-132">System.String</span><span class="sxs-lookup"><span data-stu-id="86f04-132">System.String</span></span>

### <span data-ttu-id="86f04-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="86f04-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="86f04-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86f04-134">OUTPUTS</span></span>

### <span data-ttu-id="86f04-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="86f04-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="86f04-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="86f04-136">NOTES</span></span>

## <span data-ttu-id="86f04-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86f04-137">RELATED LINKS</span></span>
