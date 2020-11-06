---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 417bc080d707c3da02dd8a0083fb707f79d0a999
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496352"
---
# <span data-ttu-id="f30b9-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="f30b9-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="f30b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f30b9-102">SYNOPSIS</span></span>
<span data-ttu-id="f30b9-103">Elindítja az IIS-naplók gyűjteményét a munkaterületen lévő számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="f30b9-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f30b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f30b9-104">SYNTAX</span></span>

### <span data-ttu-id="f30b9-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f30b9-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30b9-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f30b9-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f30b9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f30b9-107">DESCRIPTION</span></span>
<span data-ttu-id="f30b9-108">Az **enable-AzureRmOperationalInsightsIISLogCollection** parancsmag az Internet Information Services (IIS) naplóit a munkaterületen lévő csatlakoztatott számítógépekről indítja el.</span><span class="sxs-lookup"><span data-stu-id="f30b9-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="f30b9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f30b9-109">EXAMPLES</span></span>

## <span data-ttu-id="f30b9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f30b9-110">PARAMETERS</span></span>

### <span data-ttu-id="f30b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30b9-111">-DefaultProfile</span></span>
<span data-ttu-id="f30b9-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f30b9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f30b9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f30b9-113">-ResourceGroupName</span></span>
<span data-ttu-id="f30b9-114">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f30b9-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="f30b9-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="f30b9-115">-Workspace</span></span>
<span data-ttu-id="f30b9-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="f30b9-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f30b9-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f30b9-117">-WorkspaceName</span></span>
<span data-ttu-id="f30b9-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="f30b9-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f30b9-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f30b9-119">-Confirm</span></span>
<span data-ttu-id="f30b9-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f30b9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f30b9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f30b9-121">-WhatIf</span></span>
<span data-ttu-id="f30b9-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f30b9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f30b9-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f30b9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f30b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30b9-124">CommonParameters</span></span>
<span data-ttu-id="f30b9-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f30b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30b9-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f30b9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30b9-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f30b9-127">INPUTS</span></span>

### <span data-ttu-id="f30b9-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f30b9-128">PSWorkspace</span></span>
<span data-ttu-id="f30b9-129">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f30b9-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="f30b9-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f30b9-130">OUTPUTS</span></span>

### <span data-ttu-id="f30b9-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f30b9-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f30b9-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f30b9-132">NOTES</span></span>

## <span data-ttu-id="f30b9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f30b9-133">RELATED LINKS</span></span>

[<span data-ttu-id="f30b9-134">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="f30b9-134">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)


