---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: dfa855bd5bda46b6efbacdda859980036bfeb737
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672628"
---
# <span data-ttu-id="872af-101">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="872af-101">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="872af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="872af-102">SYNOPSIS</span></span>
<span data-ttu-id="872af-103">Elindítja a syslog-adatgyűjteményt a Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="872af-103">Starts collection of syslog data from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="872af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="872af-104">SYNTAX</span></span>

### <span data-ttu-id="872af-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="872af-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="872af-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="872af-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="872af-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="872af-107">DESCRIPTION</span></span>
<span data-ttu-id="872af-108">Az **enable-AzureRmOperationalInsightsLinuxSyslogCollection** parancsmag az összekapcsolt linuxos számítógépekről származó syslog-adatgyűjtést egy munkaterületről indítja el.</span><span class="sxs-lookup"><span data-stu-id="872af-108">The **Enable-AzureRmOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="872af-109">Példák</span><span class="sxs-lookup"><span data-stu-id="872af-109">EXAMPLES</span></span>

## <span data-ttu-id="872af-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="872af-110">PARAMETERS</span></span>

### <span data-ttu-id="872af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872af-111">-DefaultProfile</span></span>
<span data-ttu-id="872af-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="872af-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="872af-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="872af-113">-ResourceGroupName</span></span>
<span data-ttu-id="872af-114">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="872af-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="872af-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="872af-115">-Workspace</span></span>
<span data-ttu-id="872af-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="872af-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="872af-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="872af-117">-WorkspaceName</span></span>
<span data-ttu-id="872af-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="872af-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="872af-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="872af-119">-Confirm</span></span>
<span data-ttu-id="872af-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="872af-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="872af-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="872af-121">-WhatIf</span></span>
<span data-ttu-id="872af-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="872af-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="872af-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="872af-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="872af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872af-124">CommonParameters</span></span>
<span data-ttu-id="872af-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="872af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872af-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="872af-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872af-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="872af-127">INPUTS</span></span>

### <span data-ttu-id="872af-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="872af-128">PSWorkspace</span></span>
<span data-ttu-id="872af-129">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="872af-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="872af-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="872af-130">OUTPUTS</span></span>

### <span data-ttu-id="872af-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="872af-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="872af-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="872af-132">NOTES</span></span>
* <span data-ttu-id="872af-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="872af-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="872af-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="872af-134">RELATED LINKS</span></span>

[<span data-ttu-id="872af-135">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="872af-135">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="872af-136">Új – AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="872af-136">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


