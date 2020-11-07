---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: a730bb71ebd6f06bdae4bcbf608987a929a433c3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845222"
---
# <span data-ttu-id="2d3eb-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2d3eb-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="2d3eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d3eb-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3eb-103">Az Azure NetApp-fájlok (ANF) adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2d3eb-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="2d3eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d3eb-104">SYNTAX</span></span>

### <span data-ttu-id="2d3eb-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d3eb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d3eb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d3eb-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d3eb-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d3eb-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d3eb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d3eb-108">DESCRIPTION</span></span>
<span data-ttu-id="2d3eb-109">A **Get-AzNetAppFilesVolume** parancsmag részleteket tartalmaz a ANF-kötetekről.</span><span class="sxs-lookup"><span data-stu-id="2d3eb-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="2d3eb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2d3eb-110">EXAMPLES</span></span>

### <span data-ttu-id="2d3eb-111">Példa 1: ANF-kötet beszerzése</span><span class="sxs-lookup"><span data-stu-id="2d3eb-111">Example 1: Get an ANF volume</span></span>
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

<span data-ttu-id="2d3eb-112">Ez a parancs a MyAnfVolume nevű kötetet a "MyAnfPool" poolból kapja.</span><span class="sxs-lookup"><span data-stu-id="2d3eb-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="2d3eb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d3eb-113">PARAMETERS</span></span>

### <span data-ttu-id="2d3eb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2d3eb-114">-AccountName</span></span>
<span data-ttu-id="2d3eb-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="2d3eb-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="2d3eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d3eb-116">-DefaultProfile</span></span>
<span data-ttu-id="2d3eb-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d3eb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d3eb-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2d3eb-118">-Name</span></span>
<span data-ttu-id="2d3eb-119">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="2d3eb-119">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3eb-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2d3eb-120">-PoolName</span></span>
<span data-ttu-id="2d3eb-121">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="2d3eb-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="2d3eb-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="2d3eb-122">-PoolObject</span></span>
<span data-ttu-id="2d3eb-123">A visszaadni kívánt kötetet tartalmazó Pool objektum</span><span class="sxs-lookup"><span data-stu-id="2d3eb-123">The pool object containing the volume to return</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d3eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d3eb-125">A ANF-kötet erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="2d3eb-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="2d3eb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d3eb-126">-ResourceId</span></span>
<span data-ttu-id="2d3eb-127">A ANF-kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2d3eb-127">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3eb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3eb-128">CommonParameters</span></span>
<span data-ttu-id="2d3eb-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d3eb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2d3eb-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d3eb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3eb-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d3eb-131">INPUTS</span></span>

### <span data-ttu-id="2d3eb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2d3eb-132">System.String</span></span>

### <span data-ttu-id="2d3eb-133">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="2d3eb-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="2d3eb-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d3eb-134">OUTPUTS</span></span>

### <span data-ttu-id="2d3eb-135">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2d3eb-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2d3eb-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d3eb-136">NOTES</span></span>

## <span data-ttu-id="2d3eb-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d3eb-137">RELATED LINKS</span></span>
