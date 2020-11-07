---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 48b0fab43e104a5cae68ef26698735e89c603a78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673054"
---
# <span data-ttu-id="5d44d-101">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5d44d-101">Remove-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="5d44d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d44d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d44d-103">Állandó parancsfájl-művelet eltávolítása egy HDInsight-fürtről.</span><span class="sxs-lookup"><span data-stu-id="5d44d-103">Removes an persisted script action from an HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d44d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d44d-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d44d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d44d-105">DESCRIPTION</span></span>
<span data-ttu-id="5d44d-106">A **Remove-AzureRmHDInsightPersistedScriptAction** parancsmag egy állandó parancsfájl-műveletet távolít el a megadott Azure HDInsight-fürtök listájából, amely állandó parancsfájl-műveletekből áll.</span><span class="sxs-lookup"><span data-stu-id="5d44d-106">The **Remove-AzureRmHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="5d44d-107">Az eltávolított parancsfájl már nem fog megjelenni a fürt skálázásakor.</span><span class="sxs-lookup"><span data-stu-id="5d44d-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="5d44d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5d44d-108">EXAMPLES</span></span>

### <span data-ttu-id="5d44d-109">1. példa: parancsfájl-művelet eltávolítása a kitartott parancsfájl-műveletek listájáról a fürtökön</span><span class="sxs-lookup"><span data-stu-id="5d44d-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="5d44d-110">A parancs eltávolítja a Scriptaction nevű parancsfájl-műveletet a megadott fürt állandó parancsfájl-műveleteinek listájából.</span><span class="sxs-lookup"><span data-stu-id="5d44d-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="5d44d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d44d-111">PARAMETERS</span></span>

### <span data-ttu-id="5d44d-112">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="5d44d-112">-ClusterName</span></span>
<span data-ttu-id="5d44d-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d44d-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d44d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d44d-114">-DefaultProfile</span></span>
<span data-ttu-id="5d44d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5d44d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d44d-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d44d-116">-Name</span></span>
<span data-ttu-id="5d44d-117">Itt adhatja meg az eltávolítani kívánt állandó parancsfájl nevét.</span><span class="sxs-lookup"><span data-stu-id="5d44d-117">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d44d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d44d-118">-ResourceGroupName</span></span>
<span data-ttu-id="5d44d-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d44d-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5d44d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d44d-120">CommonParameters</span></span>
<span data-ttu-id="5d44d-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d44d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d44d-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d44d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d44d-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d44d-123">INPUTS</span></span>

### <span data-ttu-id="5d44d-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="5d44d-124">None</span></span>
<span data-ttu-id="5d44d-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5d44d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d44d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d44d-126">OUTPUTS</span></span>

### <span data-ttu-id="5d44d-127">System. Void</span><span class="sxs-lookup"><span data-stu-id="5d44d-127">System.Void</span></span>

## <span data-ttu-id="5d44d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d44d-128">NOTES</span></span>

## <span data-ttu-id="5d44d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d44d-129">RELATED LINKS</span></span>

[<span data-ttu-id="5d44d-130">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5d44d-130">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="5d44d-131">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5d44d-131">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


