---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 943edbccfa8ae8e264d4058deac0407a535c614c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010594"
---
# <span data-ttu-id="4244a-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="4244a-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="4244a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4244a-102">SYNOPSIS</span></span>
<span data-ttu-id="4244a-103">Egy vagy több szolgáltatási anyag beállítás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="4244a-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="4244a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4244a-104">SYNTAX</span></span>

### <span data-ttu-id="4244a-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="4244a-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4244a-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="4244a-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4244a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4244a-107">DESCRIPTION</span></span>
<span data-ttu-id="4244a-108">Távolítsa el a **AzServiceFabricSetting** a Service Fabric beállításaiból a fürtből.</span><span class="sxs-lookup"><span data-stu-id="4244a-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="4244a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4244a-109">EXAMPLES</span></span>

### <span data-ttu-id="4244a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4244a-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="4244a-111">Ez a parancs eltávolítja a beállítások "MaxCursors" nevű "EseStore" szakaszát.</span><span class="sxs-lookup"><span data-stu-id="4244a-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="4244a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4244a-112">PARAMETERS</span></span>

### <span data-ttu-id="4244a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4244a-113">-DefaultProfile</span></span>
<span data-ttu-id="4244a-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4244a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4244a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4244a-115">-Name</span></span>
<span data-ttu-id="4244a-116">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="4244a-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4244a-117">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="4244a-117">-Parameter</span></span>
<span data-ttu-id="4244a-118">A szövet beállítás paraméterének neve</span><span class="sxs-lookup"><span data-stu-id="4244a-118">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4244a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4244a-119">-ResourceGroupName</span></span>
<span data-ttu-id="4244a-120">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="4244a-120">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4244a-121">-Szakasz</span><span class="sxs-lookup"><span data-stu-id="4244a-121">-Section</span></span>
<span data-ttu-id="4244a-122">A szövet beállításának szakasz neve</span><span class="sxs-lookup"><span data-stu-id="4244a-122">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4244a-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="4244a-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="4244a-124">A szövet beállításainak tömbje</span><span class="sxs-lookup"><span data-stu-id="4244a-124">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4244a-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4244a-125">-Confirm</span></span>
<span data-ttu-id="4244a-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4244a-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4244a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4244a-127">-WhatIf</span></span>
<span data-ttu-id="4244a-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4244a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4244a-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4244a-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4244a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4244a-130">CommonParameters</span></span>
<span data-ttu-id="4244a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4244a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4244a-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4244a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4244a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4244a-133">INPUTS</span></span>

### <span data-ttu-id="4244a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4244a-134">System.String</span></span>

### <span data-ttu-id="4244a-135">Microsoft. Azure. Command. ServiceFabric. models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="4244a-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="4244a-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4244a-136">OUTPUTS</span></span>

### <span data-ttu-id="4244a-137">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="4244a-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4244a-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4244a-138">NOTES</span></span>

## <span data-ttu-id="4244a-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4244a-139">RELATED LINKS</span></span>
