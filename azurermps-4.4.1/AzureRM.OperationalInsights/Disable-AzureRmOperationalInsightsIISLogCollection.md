---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 9a22c275064068cff7d97d58a69e17548c764439
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494765"
---
# <span data-ttu-id="b9801-101">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="b9801-101">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="b9801-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9801-102">SYNOPSIS</span></span>
<span data-ttu-id="b9801-103">Nem állítja be az IIS-naplók gyűjteményét a számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="b9801-103">Stops collection of IIS logs from computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9801-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9801-104">SYNTAX</span></span>

### <span data-ttu-id="b9801-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9801-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9801-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b9801-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9801-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9801-107">DESCRIPTION</span></span>
<span data-ttu-id="b9801-108">A **disable-AzureRmOperationalInsightsIISLogCollection** parancsmag leállítja az Internet Information Services (IIS) naplózását egy munkaterületről csatlakoztatott számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="b9801-108">The **Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="b9801-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b9801-109">EXAMPLES</span></span>

## <span data-ttu-id="b9801-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9801-110">PARAMETERS</span></span>

### <span data-ttu-id="b9801-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9801-111">-ResourceGroupName</span></span>
<span data-ttu-id="b9801-112">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9801-112">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9801-113">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="b9801-113">-Workspace</span></span>
<span data-ttu-id="b9801-114">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="b9801-114">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9801-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b9801-115">-WorkspaceName</span></span>
<span data-ttu-id="b9801-116">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="b9801-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9801-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9801-117">-Confirm</span></span>
<span data-ttu-id="b9801-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9801-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9801-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9801-119">-WhatIf</span></span>
<span data-ttu-id="b9801-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9801-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9801-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9801-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9801-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9801-122">-DefaultProfile</span></span>
<span data-ttu-id="b9801-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9801-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9801-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9801-124">CommonParameters</span></span>
<span data-ttu-id="b9801-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9801-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9801-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9801-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9801-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9801-127">INPUTS</span></span>

### <span data-ttu-id="b9801-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b9801-128">PSWorkspace</span></span>
<span data-ttu-id="b9801-129">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b9801-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="b9801-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9801-130">OUTPUTS</span></span>

### <span data-ttu-id="b9801-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="b9801-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b9801-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9801-132">NOTES</span></span>
* <span data-ttu-id="b9801-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="b9801-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="b9801-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9801-134">RELATED LINKS</span></span>

[<span data-ttu-id="b9801-135">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="b9801-135">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Enable-AzureRmOperationalInsightsIISLogCollection.md)


