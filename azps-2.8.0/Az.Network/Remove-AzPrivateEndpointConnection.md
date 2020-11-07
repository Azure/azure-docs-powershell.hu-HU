---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9de25adae04afd0f09a2a09118c55d4e679a44db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837834"
---
# <span data-ttu-id="ca0d2-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca0d2-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="ca0d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ca0d2-103">Privát végpont-kapcsolat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="ca0d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca0d2-104">SYNTAX</span></span>

### <span data-ttu-id="ca0d2-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca0d2-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca0d2-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="ca0d2-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -Name <String> -ServiceName <String>
 -ResourceGroupName <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca0d2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca0d2-107">DESCRIPTION</span></span>
<span data-ttu-id="ca0d2-108">A **Remove-AzPrivateEndpointConnection** parancsmag a privát végpontok közötti kapcsolatot távolítja el.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span> 

## <span data-ttu-id="ca0d2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ca0d2-109">EXAMPLES</span></span>

### <span data-ttu-id="ca0d2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ca0d2-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="ca0d2-111">Ebben a példában a MyPrivateEndpointConnection1 nevű privát végpont-kapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ca0d2-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="ca0d2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca0d2-112">PARAMETERS</span></span>

### <span data-ttu-id="ca0d2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca0d2-113">-AsJob</span></span>
<span data-ttu-id="ca0d2-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ca0d2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca0d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca0d2-115">-DefaultProfile</span></span>
<span data-ttu-id="ca0d2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca0d2-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ca0d2-117">-Description</span></span>
<span data-ttu-id="ca0d2-118">A tevékenység oka.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-118">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0d2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ca0d2-119">-Force</span></span>
<span data-ttu-id="ca0d2-120">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="ca0d2-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="ca0d2-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca0d2-121">-Name</span></span>
<span data-ttu-id="ca0d2-122">A privát végpont-kapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-122">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0d2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca0d2-123">-PassThru</span></span>
<span data-ttu-id="ca0d2-124">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ca0d2-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca0d2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca0d2-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca0d2-127">A privát végpont-kapcsolat erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0d2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca0d2-128">-ResourceId</span></span>
<span data-ttu-id="ca0d2-129">A privát végpont-kapcsolat Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="ca0d2-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0d2-130">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="ca0d2-130">-ServiceName</span></span>
<span data-ttu-id="ca0d2-131">A privát végpont-kapcsolatot tartalmazó privát kapcsolat szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-131">The name of the private link service that has the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0d2-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca0d2-132">-Confirm</span></span>
<span data-ttu-id="ca0d2-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca0d2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca0d2-134">-WhatIf</span></span>
<span data-ttu-id="ca0d2-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca0d2-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca0d2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca0d2-137">CommonParameters</span></span>
<span data-ttu-id="ca0d2-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca0d2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca0d2-139">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca0d2-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca0d2-140">INPUTS</span></span>

### <span data-ttu-id="ca0d2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ca0d2-141">System.String</span></span>

## <span data-ttu-id="ca0d2-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca0d2-142">OUTPUTS</span></span>

### <span data-ttu-id="ca0d2-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca0d2-143">System.Boolean</span></span>

## <span data-ttu-id="ca0d2-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca0d2-144">NOTES</span></span>

## <span data-ttu-id="ca0d2-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca0d2-145">RELATED LINKS</span></span>

[<span data-ttu-id="ca0d2-146">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ca0d2-146">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
