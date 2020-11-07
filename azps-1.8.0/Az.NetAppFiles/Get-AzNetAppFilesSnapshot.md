---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 8f34145a65cde73ea1a5b925064c2b9a1d3f92a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670779"
---
# <span data-ttu-id="d5efa-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="d5efa-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="d5efa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5efa-102">SYNOPSIS</span></span>
<span data-ttu-id="d5efa-103">Az Azure NetApp-fájlok (ANF) pillanatképének részletei.</span><span class="sxs-lookup"><span data-stu-id="d5efa-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="d5efa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5efa-104">SYNTAX</span></span>

### <span data-ttu-id="d5efa-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5efa-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5efa-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5efa-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5efa-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5efa-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5efa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5efa-108">DESCRIPTION</span></span>
<span data-ttu-id="d5efa-109">A **Get-AzNetAppFilesSnapshot** parancsmag részleteket tartalmaz egy ANF pillanatképről.</span><span class="sxs-lookup"><span data-stu-id="d5efa-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="d5efa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d5efa-110">EXAMPLES</span></span>

### <span data-ttu-id="d5efa-111">Példa 1: ANF pillanatképének beszerzése</span><span class="sxs-lookup"><span data-stu-id="d5efa-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
CreationDate      :
ProvisioningState : Succeeded
```

<span data-ttu-id="d5efa-112">Ez a parancs a MyAnfSnapshot nevű pillanatképet a "MyAnfVolume" kötetről kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5efa-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="d5efa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5efa-113">PARAMETERS</span></span>

### <span data-ttu-id="d5efa-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d5efa-114">-AccountName</span></span>
<span data-ttu-id="d5efa-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="d5efa-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="d5efa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5efa-116">-DefaultProfile</span></span>
<span data-ttu-id="d5efa-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5efa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5efa-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5efa-118">-Name</span></span>
<span data-ttu-id="d5efa-119">A ANF pillanatképének neve</span><span class="sxs-lookup"><span data-stu-id="d5efa-119">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5efa-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d5efa-120">-PoolName</span></span>
<span data-ttu-id="d5efa-121">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="d5efa-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d5efa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5efa-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5efa-123">A ANF-kötet erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="d5efa-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="d5efa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5efa-124">-ResourceId</span></span>
<span data-ttu-id="d5efa-125">A ANF pillanatképének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d5efa-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="d5efa-126">-Kötetnév</span><span class="sxs-lookup"><span data-stu-id="d5efa-126">-VolumeName</span></span>
<span data-ttu-id="d5efa-127">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="d5efa-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="d5efa-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="d5efa-128">-VolumeObject</span></span>
<span data-ttu-id="d5efa-129">A visszaadni kívánt pillanatképet tartalmazó mennyiségi objektum</span><span class="sxs-lookup"><span data-stu-id="d5efa-129">The volume object containing the snapshot to return</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5efa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5efa-130">CommonParameters</span></span>
<span data-ttu-id="d5efa-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5efa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d5efa-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5efa-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5efa-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5efa-133">INPUTS</span></span>

### <span data-ttu-id="d5efa-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d5efa-134">System.String</span></span>

### <span data-ttu-id="d5efa-135">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d5efa-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d5efa-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5efa-136">OUTPUTS</span></span>

### <span data-ttu-id="d5efa-137">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="d5efa-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="d5efa-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5efa-138">NOTES</span></span>

## <span data-ttu-id="d5efa-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5efa-139">RELATED LINKS</span></span>
