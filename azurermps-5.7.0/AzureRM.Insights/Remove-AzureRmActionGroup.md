---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 1d4a5365ac2112364a544eb2481a3193f23519c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500591"
---
# <span data-ttu-id="7f120-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="7f120-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="7f120-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f120-102">SYNOPSIS</span></span>
<span data-ttu-id="7f120-103">Egy művelet csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="7f120-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f120-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f120-104">SYNTAX</span></span>

### <span data-ttu-id="7f120-105">ByPropertyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f120-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f120-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f120-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f120-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7f120-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f120-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f120-108">DESCRIPTION</span></span>
<span data-ttu-id="7f120-109">A **Remove-AzureRmActionGroup** parancsmag eltávolítja a művelet csoportját.</span><span class="sxs-lookup"><span data-stu-id="7f120-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="7f120-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7f120-110">EXAMPLES</span></span>

### <span data-ttu-id="7f120-111">1. példa: a műveleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7f120-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="7f120-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f120-112">PARAMETERS</span></span>

### <span data-ttu-id="7f120-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f120-113">-DefaultProfile</span></span>
<span data-ttu-id="7f120-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f120-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f120-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f120-115">-InputObject</span></span>
<span data-ttu-id="7f120-116">A műveleti csoport resourc</span><span class="sxs-lookup"><span data-stu-id="7f120-116">The action group resourc</span></span>

```yaml
Type: PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7f120-117">-Name</span></span>
<span data-ttu-id="7f120-118">A műveleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7f120-118">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f120-119">-ResourceGroupName</span></span>
<span data-ttu-id="7f120-120">A Nam erőforrás csoport</span><span class="sxs-lookup"><span data-stu-id="7f120-120">The resource group nam</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f120-121">-ResourceId</span></span>
<span data-ttu-id="7f120-122">Az erőforrás i</span><span class="sxs-lookup"><span data-stu-id="7f120-122">The resource i</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7f120-123">-Confirm</span></span>
<span data-ttu-id="7f120-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7f120-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f120-125">-WhatIf</span></span>
<span data-ttu-id="7f120-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7f120-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f120-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f120-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f120-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f120-128">CommonParameters</span></span>
<span data-ttu-id="7f120-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f120-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f120-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f120-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f120-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f120-131">INPUTS</span></span>

### <span data-ttu-id="7f120-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="7f120-132">None</span></span>
<span data-ttu-id="7f120-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7f120-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f120-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f120-134">OUTPUTS</span></span>

### <span data-ttu-id="7f120-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7f120-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="7f120-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f120-136">NOTES</span></span>

## <span data-ttu-id="7f120-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f120-137">RELATED LINKS</span></span>

<span data-ttu-id="7f120-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Új – AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="7f120-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
