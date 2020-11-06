---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: 4c71a5b71c04c8593443820989c935852b8a002b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496995"
---
# <span data-ttu-id="bdaf0-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="bdaf0-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="bdaf0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bdaf0-102">SYNOPSIS</span></span>
<span data-ttu-id="bdaf0-103">Egyéni naplózási házirendet határoz meg.</span><span class="sxs-lookup"><span data-stu-id="bdaf0-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdaf0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bdaf0-104">SYNTAX</span></span>

### <span data-ttu-id="bdaf0-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bdaf0-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdaf0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bdaf0-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdaf0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bdaf0-107">DESCRIPTION</span></span>
<span data-ttu-id="bdaf0-108">A **New-AzureRmOperationalInsightsCustomLogDataSource** parancsmag egyéni naplózási házirendet határoz meg.</span><span class="sxs-lookup"><span data-stu-id="bdaf0-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="bdaf0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bdaf0-109">EXAMPLES</span></span>

## <span data-ttu-id="bdaf0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bdaf0-110">PARAMETERS</span></span>

### <span data-ttu-id="bdaf0-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="bdaf0-111">-CustomLogRawJson</span></span>
<span data-ttu-id="bdaf0-112">Az egyéni webhelycsoport-házirendet adja meg nyers JavaScript-objektumként (JSON) karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="bdaf0-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdaf0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bdaf0-113">-Force</span></span>
<span data-ttu-id="bdaf0-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="bdaf0-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdaf0-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bdaf0-115">-Name</span></span>
<span data-ttu-id="bdaf0-116">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdaf0-116">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdaf0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdaf0-117">-ResourceGroupName</span></span>
<span data-ttu-id="bdaf0-118">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdaf0-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="bdaf0-119">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="bdaf0-119">-Workspace</span></span>
<span data-ttu-id="bdaf0-120">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="bdaf0-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bdaf0-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bdaf0-121">-WorkspaceName</span></span>
<span data-ttu-id="bdaf0-122">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="bdaf0-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bdaf0-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bdaf0-123">-Confirm</span></span>
<span data-ttu-id="bdaf0-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bdaf0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdaf0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdaf0-125">-WhatIf</span></span>
<span data-ttu-id="bdaf0-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bdaf0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdaf0-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bdaf0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdaf0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdaf0-128">-DefaultProfile</span></span>
<span data-ttu-id="bdaf0-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdaf0-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdaf0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdaf0-130">CommonParameters</span></span>
<span data-ttu-id="bdaf0-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bdaf0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdaf0-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdaf0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdaf0-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdaf0-133">INPUTS</span></span>

### <span data-ttu-id="bdaf0-134">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bdaf0-134">PSWorkspace</span></span>
<span data-ttu-id="bdaf0-135">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="bdaf0-135">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="bdaf0-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdaf0-136">OUTPUTS</span></span>

### <span data-ttu-id="bdaf0-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bdaf0-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bdaf0-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bdaf0-138">NOTES</span></span>

## <span data-ttu-id="bdaf0-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdaf0-139">RELATED LINKS</span></span>

[<span data-ttu-id="bdaf0-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bdaf0-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="bdaf0-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bdaf0-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


