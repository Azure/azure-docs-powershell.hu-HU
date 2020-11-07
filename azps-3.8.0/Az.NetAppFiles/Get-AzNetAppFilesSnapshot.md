---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: b41acc1d10a09febec04b60c397496b97606fb18
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845062"
---
# <span data-ttu-id="15a5a-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="15a5a-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="15a5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="15a5a-103">Az Azure NetApp-fájlok (ANF) pillanatképének részletei.</span><span class="sxs-lookup"><span data-stu-id="15a5a-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="15a5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15a5a-104">SYNTAX</span></span>

### <span data-ttu-id="15a5a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15a5a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15a5a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15a5a-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15a5a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15a5a-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15a5a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="15a5a-108">DESCRIPTION</span></span>
<span data-ttu-id="15a5a-109">A **Get-AzNetAppFilesSnapshot** parancsmag részleteket tartalmaz egy ANF pillanatképről.</span><span class="sxs-lookup"><span data-stu-id="15a5a-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="15a5a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="15a5a-110">EXAMPLES</span></span>

### <span data-ttu-id="15a5a-111">Példa 1: ANF pillanatképének beszerzése</span><span class="sxs-lookup"><span data-stu-id="15a5a-111">Example 1: Get an ANF snapshot</span></span>
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
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="15a5a-112">Ez a parancs a MyAnfSnapshot nevű pillanatképet a "MyAnfVolume" kötetről kapja meg.</span><span class="sxs-lookup"><span data-stu-id="15a5a-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="15a5a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15a5a-113">PARAMETERS</span></span>

### <span data-ttu-id="15a5a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="15a5a-114">-AccountName</span></span>
<span data-ttu-id="15a5a-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="15a5a-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="15a5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a5a-116">-DefaultProfile</span></span>
<span data-ttu-id="15a5a-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15a5a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a5a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="15a5a-118">-Name</span></span>
<span data-ttu-id="15a5a-119">A ANF pillanatképének neve</span><span class="sxs-lookup"><span data-stu-id="15a5a-119">The name of the ANF snapshot</span></span>

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

### <span data-ttu-id="15a5a-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="15a5a-120">-PoolName</span></span>
<span data-ttu-id="15a5a-121">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="15a5a-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="15a5a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a5a-122">-ResourceGroupName</span></span>
<span data-ttu-id="15a5a-123">A ANF-kötet erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="15a5a-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="15a5a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15a5a-124">-ResourceId</span></span>
<span data-ttu-id="15a5a-125">A ANF pillanatképének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="15a5a-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="15a5a-126">-Kötetnév</span><span class="sxs-lookup"><span data-stu-id="15a5a-126">-VolumeName</span></span>
<span data-ttu-id="15a5a-127">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="15a5a-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="15a5a-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="15a5a-128">-VolumeObject</span></span>
<span data-ttu-id="15a5a-129">A visszaadni kívánt pillanatképet tartalmazó mennyiségi objektum</span><span class="sxs-lookup"><span data-stu-id="15a5a-129">The volume object containing the snapshot to return</span></span>

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

### <span data-ttu-id="15a5a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a5a-130">CommonParameters</span></span>
<span data-ttu-id="15a5a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15a5a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="15a5a-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a5a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a5a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15a5a-133">INPUTS</span></span>

### <span data-ttu-id="15a5a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="15a5a-134">System.String</span></span>

### <span data-ttu-id="15a5a-135">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="15a5a-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="15a5a-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15a5a-136">OUTPUTS</span></span>

### <span data-ttu-id="15a5a-137">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="15a5a-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="15a5a-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15a5a-138">NOTES</span></span>

## <span data-ttu-id="15a5a-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15a5a-139">RELATED LINKS</span></span>
