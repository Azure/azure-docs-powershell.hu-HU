---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015720"
---
# <span data-ttu-id="d1b2d-101">Add-AzureHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="d1b2d-101">Add-AzureHDInsightScriptAction</span></span>

## <span data-ttu-id="d1b2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b2d-103">Egy HDInsight parancsfájl-művelet hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d1b2d-103">Adds an HDInsight script action.</span></span>

## <span data-ttu-id="d1b2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1b2d-104">SYNTAX</span></span>

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1b2d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1b2d-105">DESCRIPTION</span></span>
<span data-ttu-id="d1b2d-106">Az Azure PowerShell HDInsight ez a verziója elavult.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="d1b2d-107">A következő parancsmagok törlődnek január 1, 2017.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="d1b2d-108">Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="d1b2d-109">Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="d1b2d-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="d1b2d-110">Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)</span><span class="sxs-lookup"><span data-stu-id="d1b2d-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="d1b2d-111">Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d1b2d-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="d1b2d-112">A **Add-AzureHDInsightScriptAction** parancsmag Azure HDInsight funkciókat biztosít, amelyek a további szoftverek telepítéséhez vagy a Hadoop-fürtökön futó alkalmazások konfigurációjának módosításához használhatók a Windows PowerShell-parancsfájlok használatával.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-112">The **Add-AzureHDInsightScriptAction** cmdlet provides Azure HDInsight functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell scripts.</span></span>

<span data-ttu-id="d1b2d-113">Parancsfájl-műveletek akkor futnak a fürtcsomópontok során, ha a HDInsight-fürtöket telepítik, és a fürt a fürtök teljes HDInsight-konfigurációját követően futnak.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-113">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="d1b2d-114">A parancsfájl-műveletek a rendszeradminisztrátori fiók jogosultságai csoportban futnak, és teljes hozzáférési jogosultságokat biztosítanak a fürtcsomópontok számára.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-114">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="d1b2d-115">Az egyes fürtöket megadhatja az adott sorrendben futtatandó parancsfájl-műveletek listájával.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-115">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="d1b2d-116">Példák</span><span class="sxs-lookup"><span data-stu-id="d1b2d-116">EXAMPLES</span></span>

### <span data-ttu-id="d1b2d-117">1. példa: parancsfájl-művelet hozzáadása fürthöz</span><span class="sxs-lookup"><span data-stu-id="d1b2d-117">Example 1: Add a script action to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="d1b2d-118">Az első parancs a **New-AzureHDInsightClusterConfig** parancsmagot használja az HDInsight-beli fürtkonfiguráció létrehozásához, majd a $config változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-118">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="d1b2d-119">A második parancs az **Add-AzureHDInsightScriptAction** parancsmagot használja a TestScriptAction nevű parancsfájl-műveletek hozzáadásához a $config.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-119">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the script action named TestScriptAction to $Config.</span></span>

<span data-ttu-id="d1b2d-120">A végleges parancs a **New-AzureHDInsightCluster** parancsmagot használja az $config-ban tárolt parancsfájlokat futtató új HDInsight-fürtök létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-120">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster that runs the script action stored in $Config.</span></span>

### <span data-ttu-id="d1b2d-121">2. példa: több parancsfájl-művelet hozzáadása a fürthöz</span><span class="sxs-lookup"><span data-stu-id="d1b2d-121">Example 2: Add multiple script actions to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="d1b2d-122">Az első parancs a **New-AzureHDInsightClusterConfig** parancsmagot használja az HDInsight-beli fürtkonfiguráció létrehozásához, majd a $config változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-122">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="d1b2d-123">A második parancs az **Add-AzureHDInsightScriptAction** parancsmaggal adja hozzá a megadott parancsfájl-műveletet az $Confighez, és a pipeline operátor segítségével másodszor is felveszi a $Configt, ha második parancsfájl **-** műveletet szeretne hozzáadni a $Confighoz.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-123">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the specified script action to $Config, and then uses the pipeline operator to pass $Config to **Add-AzureHDInsightScriptAction** a second time to add a second script action to $Config.</span></span>

<span data-ttu-id="d1b2d-124">A végleges parancs a **New-AzureHDInsightCluster** parancsmagot használja az $config parancsfájl-műveleteket futtató fürtök létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-124">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a cluster that runs the script actions in $Config.</span></span>

## <span data-ttu-id="d1b2d-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1b2d-125">PARAMETERS</span></span>

### <span data-ttu-id="d1b2d-126">-ClusterRoleCollection</span><span class="sxs-lookup"><span data-stu-id="d1b2d-126">-ClusterRoleCollection</span></span>
<span data-ttu-id="d1b2d-127">Azokat a csomópontokat adja meg, amelyekhez parancsfájlt kell futtatni.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-127">Specifies the nodes for which to run a script.</span></span>
<span data-ttu-id="d1b2d-128">A paraméter elfogadható értékei a következők: HeadNode vagy DataNode.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-128">The acceptable values for this parameter are: HeadNode or DataNode.</span></span>

<span data-ttu-id="d1b2d-129">Adhat meg egy értéket vagy mindkét értéket.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-129">You can specify one value or both values.</span></span>

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b2d-130">-Config</span><span class="sxs-lookup"><span data-stu-id="d1b2d-130">-Config</span></span>
<span data-ttu-id="d1b2d-131">Konfigurációs objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-131">Specifies a configuration object.</span></span>
<span data-ttu-id="d1b2d-132">Ez a parancsmag parancsfájl-műveleti információkat ad az objektumhoz, amelyhez ez a paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-132">This cmdlet adds script action information to the object that this parameter specifies.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1b2d-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d1b2d-133">-Name</span></span>
<span data-ttu-id="d1b2d-134">A parancsfájl-műveletek nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-134">Specifies the name of a script action.</span></span>

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

### <span data-ttu-id="d1b2d-135">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="d1b2d-135">-Parameters</span></span>
<span data-ttu-id="d1b2d-136">A parancsfájl-műveletek által megkövetelt paramétereket adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-136">Specifies the parameters that are required by a script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b2d-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="d1b2d-137">-Profile</span></span>
<span data-ttu-id="d1b2d-138">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d1b2d-139">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b2d-140">-URI</span><span class="sxs-lookup"><span data-stu-id="d1b2d-140">-Uri</span></span>
<span data-ttu-id="d1b2d-141">A futtatandó parancsfájl URI-helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1b2d-141">Specifies the URI location of a script to run.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b2d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b2d-142">CommonParameters</span></span>
<span data-ttu-id="d1b2d-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1b2d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b2d-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1b2d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b2d-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1b2d-145">INPUTS</span></span>

## <span data-ttu-id="d1b2d-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1b2d-146">OUTPUTS</span></span>

## <span data-ttu-id="d1b2d-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1b2d-147">NOTES</span></span>

## <span data-ttu-id="d1b2d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1b2d-148">RELATED LINKS</span></span>

[<span data-ttu-id="d1b2d-149">Új – AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d1b2d-149">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="d1b2d-150">Új – AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d1b2d-150">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


