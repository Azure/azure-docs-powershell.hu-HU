---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 0b5f84a38fcd087b77b32624b9cbd9b3b8a27e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680267"
---
# <span data-ttu-id="0f521-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="0f521-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="0f521-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f521-102">SYNOPSIS</span></span>
<span data-ttu-id="0f521-103">Egy művelet csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0f521-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f521-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f521-104">SYNTAX</span></span>

### <span data-ttu-id="0f521-105">ByPropertyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f521-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f521-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f521-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f521-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f521-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f521-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f521-108">DESCRIPTION</span></span>
<span data-ttu-id="0f521-109">A **Remove-AzureRmActionGroup** parancsmag eltávolítja a művelet csoportját.</span><span class="sxs-lookup"><span data-stu-id="0f521-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="0f521-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0f521-110">EXAMPLES</span></span>

### <span data-ttu-id="0f521-111">1. példa: a műveleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0f521-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="0f521-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f521-112">PARAMETERS</span></span>

### <span data-ttu-id="0f521-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f521-113">-Name</span></span>
<span data-ttu-id="0f521-114">A műveleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0f521-114">The name of the action group.</span></span>

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

### <span data-ttu-id="0f521-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f521-115">-Confirm</span></span>
<span data-ttu-id="0f521-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f521-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f521-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f521-117">-DefaultProfile</span></span>
<span data-ttu-id="0f521-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f521-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f521-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f521-119">-InputObject</span></span>
<span data-ttu-id="0f521-120">A műveleti csoport erőforrás</span><span class="sxs-lookup"><span data-stu-id="0f521-120">The action group resource</span></span>

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

### <span data-ttu-id="0f521-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f521-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f521-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0f521-122">The resource group name</span></span>

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

### <span data-ttu-id="0f521-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f521-123">-ResourceId</span></span>
<span data-ttu-id="0f521-124">Az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="0f521-124">The resource id</span></span>

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

### <span data-ttu-id="0f521-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f521-125">-WhatIf</span></span>
<span data-ttu-id="0f521-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f521-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f521-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f521-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f521-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f521-128">CommonParameters</span></span>
<span data-ttu-id="0f521-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f521-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f521-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f521-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f521-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f521-131">INPUTS</span></span>

## <span data-ttu-id="0f521-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f521-132">OUTPUTS</span></span>

### <span data-ttu-id="0f521-133">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0f521-133">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0f521-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f521-134">NOTES</span></span>

## <span data-ttu-id="0f521-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f521-135">RELATED LINKS</span></span>

<span data-ttu-id="0f521-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Új – AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="0f521-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
