---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 3fdd6b407753e8edd9ba7faa074e287062f15fb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494022"
---
# <span data-ttu-id="8c012-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="8c012-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="8c012-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c012-102">SYNOPSIS</span></span>
<span data-ttu-id="8c012-103">Nem állítja be a syslog-adatgyűjtést a Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="8c012-103">Stops collection of syslog data from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c012-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c012-104">SYNTAX</span></span>

### <span data-ttu-id="8c012-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c012-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c012-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8c012-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c012-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c012-107">DESCRIPTION</span></span>
<span data-ttu-id="8c012-108">A **disable-AzureRmOperationalInsightsLinuxSyslogCollection** parancsmag nem gyűjti össze a syslog-adatforrásokat a csatlakoztatott linuxos számítógépekről egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="8c012-108">The **Disable-AzureRmOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="8c012-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8c012-109">EXAMPLES</span></span>

## <span data-ttu-id="8c012-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c012-110">PARAMETERS</span></span>

### <span data-ttu-id="8c012-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c012-111">-DefaultProfile</span></span>
<span data-ttu-id="8c012-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8c012-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c012-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c012-113">-ResourceGroupName</span></span>
<span data-ttu-id="8c012-114">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c012-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="8c012-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="8c012-115">-Workspace</span></span>
<span data-ttu-id="8c012-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="8c012-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8c012-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8c012-117">-WorkspaceName</span></span>
<span data-ttu-id="8c012-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="8c012-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8c012-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8c012-119">-Confirm</span></span>
<span data-ttu-id="8c012-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c012-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c012-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c012-121">-WhatIf</span></span>
<span data-ttu-id="8c012-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8c012-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c012-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c012-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c012-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c012-124">CommonParameters</span></span>
<span data-ttu-id="8c012-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c012-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c012-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c012-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c012-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c012-127">INPUTS</span></span>

### <span data-ttu-id="8c012-128">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8c012-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="8c012-129">Paraméterek: munkaterület (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8c012-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="8c012-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8c012-130">System.String</span></span>

## <span data-ttu-id="8c012-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c012-131">OUTPUTS</span></span>

### <span data-ttu-id="8c012-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="8c012-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8c012-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c012-133">NOTES</span></span>
* <span data-ttu-id="8c012-134">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="8c012-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="8c012-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c012-135">RELATED LINKS</span></span>

[<span data-ttu-id="8c012-136">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="8c012-136">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="8c012-137">Új – AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="8c012-137">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


