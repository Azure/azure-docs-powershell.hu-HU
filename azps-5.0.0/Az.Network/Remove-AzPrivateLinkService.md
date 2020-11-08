---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188243"
---
# <span data-ttu-id="61e08-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="61e08-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="61e08-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61e08-102">SYNOPSIS</span></span>
<span data-ttu-id="61e08-103">Privát link szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="61e08-103">Removes a private link service</span></span>

## <span data-ttu-id="61e08-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61e08-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61e08-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="61e08-105">DESCRIPTION</span></span>
<span data-ttu-id="61e08-106">A **Remove-AzPrivateLinkService** parancsmag eltávolítja a privát hivatkozás szolgáltatást</span><span class="sxs-lookup"><span data-stu-id="61e08-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="61e08-107">Példák</span><span class="sxs-lookup"><span data-stu-id="61e08-107">EXAMPLES</span></span>

### <span data-ttu-id="61e08-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="61e08-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="61e08-109">Ez a példa eltávolítja a TestPrivateLinkService nevű privát hivatkozás szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="61e08-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="61e08-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61e08-110">PARAMETERS</span></span>

### <span data-ttu-id="61e08-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61e08-111">-AsJob</span></span>
<span data-ttu-id="61e08-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="61e08-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61e08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e08-113">-DefaultProfile</span></span>
<span data-ttu-id="61e08-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61e08-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61e08-115">-Force</span><span class="sxs-lookup"><span data-stu-id="61e08-115">-Force</span></span>
<span data-ttu-id="61e08-116">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="61e08-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="61e08-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="61e08-117">-Name</span></span>
<span data-ttu-id="61e08-118">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="61e08-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e08-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61e08-119">-PassThru</span></span>
<span data-ttu-id="61e08-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="61e08-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="61e08-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="61e08-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="61e08-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61e08-122">-ResourceGroupName</span></span>
<span data-ttu-id="61e08-123">A privát kapcsolat szolgáltatás erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="61e08-123">The resource group name of the private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e08-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="61e08-124">-Confirm</span></span>
<span data-ttu-id="61e08-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="61e08-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61e08-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e08-126">-WhatIf</span></span>
<span data-ttu-id="61e08-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="61e08-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61e08-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="61e08-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61e08-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e08-129">CommonParameters</span></span>
<span data-ttu-id="61e08-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61e08-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e08-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="61e08-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e08-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61e08-132">INPUTS</span></span>

### <span data-ttu-id="61e08-133">System. String</span><span class="sxs-lookup"><span data-stu-id="61e08-133">System.String</span></span>

## <span data-ttu-id="61e08-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61e08-134">OUTPUTS</span></span>

### <span data-ttu-id="61e08-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61e08-135">System.Boolean</span></span>

## <span data-ttu-id="61e08-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61e08-136">NOTES</span></span>

## <span data-ttu-id="61e08-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61e08-137">RELATED LINKS</span></span>

[<span data-ttu-id="61e08-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="61e08-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="61e08-139">Új – AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="61e08-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)