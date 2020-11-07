---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7ec50b0698017c20fb47030ccb571d6b4083b97b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849322"
---
# <span data-ttu-id="2809b-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="2809b-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="2809b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2809b-102">SYNOPSIS</span></span>
<span data-ttu-id="2809b-103">Egy művelet csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2809b-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2809b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2809b-104">SYNTAX</span></span>

### <span data-ttu-id="2809b-105">ByPropertyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2809b-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2809b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2809b-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2809b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2809b-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2809b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2809b-108">DESCRIPTION</span></span>
<span data-ttu-id="2809b-109">A **Remove-AzureRmActionGroup** parancsmag eltávolítja a művelet csoportját.</span><span class="sxs-lookup"><span data-stu-id="2809b-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="2809b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2809b-110">EXAMPLES</span></span>

### <span data-ttu-id="2809b-111">1. példa: a műveleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2809b-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="2809b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2809b-112">PARAMETERS</span></span>

### <span data-ttu-id="2809b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2809b-113">-DefaultProfile</span></span>
<span data-ttu-id="2809b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2809b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2809b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2809b-115">-InputObject</span></span>
<span data-ttu-id="2809b-116">A műveleti csoport resourc</span><span class="sxs-lookup"><span data-stu-id="2809b-116">The action group resourc</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2809b-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2809b-117">-Name</span></span>
<span data-ttu-id="2809b-118">A műveleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2809b-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2809b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2809b-119">-ResourceGroupName</span></span>
<span data-ttu-id="2809b-120">A Nam erőforrás csoport</span><span class="sxs-lookup"><span data-stu-id="2809b-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2809b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2809b-121">-ResourceId</span></span>
<span data-ttu-id="2809b-122">Az erőforrás i</span><span class="sxs-lookup"><span data-stu-id="2809b-122">The resource i</span></span>

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

### <span data-ttu-id="2809b-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2809b-123">-Confirm</span></span>
<span data-ttu-id="2809b-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2809b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2809b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2809b-125">-WhatIf</span></span>
<span data-ttu-id="2809b-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2809b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2809b-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2809b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2809b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2809b-128">CommonParameters</span></span>
<span data-ttu-id="2809b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2809b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2809b-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2809b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2809b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2809b-131">INPUTS</span></span>

### <span data-ttu-id="2809b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2809b-132">System.String</span></span>

### <span data-ttu-id="2809b-133">Microsoft. Azure. commands. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="2809b-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="2809b-134">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2809b-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2809b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2809b-135">OUTPUTS</span></span>

### <span data-ttu-id="2809b-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2809b-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2809b-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2809b-137">NOTES</span></span>

## <span data-ttu-id="2809b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2809b-138">RELATED LINKS</span></span>

<span data-ttu-id="2809b-139">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Új – AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="2809b-139">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
