---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 3b0ba9527ca7d0354429a90439bbe33d973bf550
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837087"
---
# <span data-ttu-id="19945-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="19945-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="19945-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19945-102">SYNOPSIS</span></span>
<span data-ttu-id="19945-103">Privát link szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="19945-103">Removes a private link service</span></span>

## <span data-ttu-id="19945-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19945-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19945-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19945-105">DESCRIPTION</span></span>
<span data-ttu-id="19945-106">A **Remove-AzPrivateLinkService** parancsmag eltávolítja a privát hivatkozás szolgáltatást</span><span class="sxs-lookup"><span data-stu-id="19945-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="19945-107">Példák</span><span class="sxs-lookup"><span data-stu-id="19945-107">EXAMPLES</span></span>

### <span data-ttu-id="19945-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19945-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="19945-109">Ez a példa eltávolítja a TestPrivateLinkService nevű privát hivatkozás szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="19945-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="19945-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19945-110">PARAMETERS</span></span>

### <span data-ttu-id="19945-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19945-111">-AsJob</span></span>
<span data-ttu-id="19945-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="19945-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19945-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19945-113">-DefaultProfile</span></span>
<span data-ttu-id="19945-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19945-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19945-115">-Force</span><span class="sxs-lookup"><span data-stu-id="19945-115">-Force</span></span>
<span data-ttu-id="19945-116">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="19945-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="19945-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19945-117">-Name</span></span>
<span data-ttu-id="19945-118">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="19945-118">The name of the service.</span></span>

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

### <span data-ttu-id="19945-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19945-119">-PassThru</span></span>
<span data-ttu-id="19945-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="19945-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="19945-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="19945-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="19945-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19945-122">-ResourceGroupName</span></span>
<span data-ttu-id="19945-123">A privát kapcsolat szolgáltatás erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="19945-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="19945-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19945-124">-Confirm</span></span>
<span data-ttu-id="19945-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19945-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19945-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19945-126">-WhatIf</span></span>
<span data-ttu-id="19945-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19945-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19945-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19945-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19945-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19945-129">CommonParameters</span></span>
<span data-ttu-id="19945-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19945-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19945-131">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="19945-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19945-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19945-132">INPUTS</span></span>

### <span data-ttu-id="19945-133">System. String</span><span class="sxs-lookup"><span data-stu-id="19945-133">System.String</span></span>

## <span data-ttu-id="19945-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19945-134">OUTPUTS</span></span>

### <span data-ttu-id="19945-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19945-135">System.Boolean</span></span>

## <span data-ttu-id="19945-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19945-136">NOTES</span></span>

## <span data-ttu-id="19945-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19945-137">RELATED LINKS</span></span>

[<span data-ttu-id="19945-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="19945-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="19945-139">Új – AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="19945-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)