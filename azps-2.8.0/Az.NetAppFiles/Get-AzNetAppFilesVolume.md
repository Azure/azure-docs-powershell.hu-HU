---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 3d44c9def7dd56fa0d3fa58fd417a738c5db051b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837713"
---
# <span data-ttu-id="2eb18-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2eb18-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="2eb18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2eb18-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb18-103">Az Azure NetApp-fájlok (ANF) adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2eb18-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="2eb18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2eb18-104">SYNTAX</span></span>

### <span data-ttu-id="2eb18-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2eb18-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb18-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2eb18-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb18-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2eb18-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2eb18-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2eb18-108">DESCRIPTION</span></span>
<span data-ttu-id="2eb18-109">A **Get-AzNetAppFilesVolume** parancsmag részleteket tartalmaz a ANF-kötetekről.</span><span class="sxs-lookup"><span data-stu-id="2eb18-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="2eb18-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2eb18-110">EXAMPLES</span></span>

### <span data-ttu-id="2eb18-111">Példa 1: ANF-kötet beszerzése</span><span class="sxs-lookup"><span data-stu-id="2eb18-111">Example 1: Get an ANF volume</span></span>
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

<span data-ttu-id="2eb18-112">Ez a parancs a MyAnfVolume nevű kötetet a "MyAnfPool" poolból kapja.</span><span class="sxs-lookup"><span data-stu-id="2eb18-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="2eb18-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2eb18-113">PARAMETERS</span></span>

### <span data-ttu-id="2eb18-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2eb18-114">-AccountName</span></span>
<span data-ttu-id="2eb18-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="2eb18-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="2eb18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb18-116">-DefaultProfile</span></span>
<span data-ttu-id="2eb18-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2eb18-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eb18-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2eb18-118">-Name</span></span>
<span data-ttu-id="2eb18-119">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="2eb18-119">The name of the ANF volume</span></span>

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

### <span data-ttu-id="2eb18-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2eb18-120">-PoolName</span></span>
<span data-ttu-id="2eb18-121">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="2eb18-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="2eb18-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="2eb18-122">-PoolObject</span></span>
<span data-ttu-id="2eb18-123">A visszaadni kívánt kötetet tartalmazó Pool objektum</span><span class="sxs-lookup"><span data-stu-id="2eb18-123">The pool object containing the volume to return</span></span>

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

### <span data-ttu-id="2eb18-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb18-124">-ResourceGroupName</span></span>
<span data-ttu-id="2eb18-125">A ANF-kötet erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="2eb18-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="2eb18-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2eb18-126">-ResourceId</span></span>
<span data-ttu-id="2eb18-127">A ANF-kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2eb18-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="2eb18-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb18-128">CommonParameters</span></span>
<span data-ttu-id="2eb18-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2eb18-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2eb18-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eb18-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb18-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2eb18-131">INPUTS</span></span>

### <span data-ttu-id="2eb18-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2eb18-132">System.String</span></span>

### <span data-ttu-id="2eb18-133">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="2eb18-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="2eb18-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2eb18-134">OUTPUTS</span></span>

### <span data-ttu-id="2eb18-135">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2eb18-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2eb18-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2eb18-136">NOTES</span></span>

## <span data-ttu-id="2eb18-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2eb18-137">RELATED LINKS</span></span>
