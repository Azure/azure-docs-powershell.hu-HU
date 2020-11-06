---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 99ec8caac4a4e5d2dfab6b881bb32eee62a90371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496347"
---
# <span data-ttu-id="a643c-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="a643c-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="a643c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a643c-102">SYNOPSIS</span></span>
<span data-ttu-id="a643c-103">Elindítja a teljesítményszámlálók gyűjteményét a Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="a643c-103">Starts collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a643c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a643c-104">SYNTAX</span></span>

### <span data-ttu-id="a643c-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a643c-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a643c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a643c-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a643c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a643c-107">DESCRIPTION</span></span>
<span data-ttu-id="a643c-108">Az **enable-AzureRmOperationalInsightsLinuxPerformanceCollection** parancsmag a csatlakoztatott linuxos számítógépekről származó teljesítményszámlálók gyűjteményét indítja el egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="a643c-108">The **Enable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="a643c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a643c-109">EXAMPLES</span></span>

## <span data-ttu-id="a643c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a643c-110">PARAMETERS</span></span>

### <span data-ttu-id="a643c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a643c-111">-DefaultProfile</span></span>
<span data-ttu-id="a643c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a643c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a643c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a643c-113">-ResourceGroupName</span></span>
<span data-ttu-id="a643c-114">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a643c-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a643c-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="a643c-115">-Workspace</span></span>
<span data-ttu-id="a643c-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="a643c-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a643c-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a643c-117">-WorkspaceName</span></span>
<span data-ttu-id="a643c-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="a643c-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a643c-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a643c-119">-Confirm</span></span>
<span data-ttu-id="a643c-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a643c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a643c-121">-WhatIf</span></span>
<span data-ttu-id="a643c-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a643c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a643c-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a643c-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a643c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a643c-124">CommonParameters</span></span>
<span data-ttu-id="a643c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a643c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a643c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a643c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a643c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a643c-127">INPUTS</span></span>

### <span data-ttu-id="a643c-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a643c-128">PSWorkspace</span></span>
<span data-ttu-id="a643c-129">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a643c-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="a643c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a643c-130">OUTPUTS</span></span>

### <span data-ttu-id="a643c-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a643c-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a643c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a643c-132">NOTES</span></span>
* <span data-ttu-id="a643c-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="a643c-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="a643c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a643c-134">RELATED LINKS</span></span>

[<span data-ttu-id="a643c-135">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="a643c-135">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


