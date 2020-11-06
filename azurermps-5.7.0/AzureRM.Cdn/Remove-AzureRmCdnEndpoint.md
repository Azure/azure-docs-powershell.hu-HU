---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 8748806346baa4f84550d15749e7792ae928ad34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495469"
---
# <span data-ttu-id="45ea6-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="45ea6-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="45ea6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="45ea6-103">Egy CDN-végpont eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="45ea6-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45ea6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45ea6-104">SYNTAX</span></span>

### <span data-ttu-id="45ea6-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="45ea6-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ea6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45ea6-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45ea6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="45ea6-107">DESCRIPTION</span></span>
<span data-ttu-id="45ea6-108">A **Remove-AzureRmCdnEndpoint** parancsmag eltávolítja az Azure Content Delivery Network (CDN) végpontját.</span><span class="sxs-lookup"><span data-stu-id="45ea6-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="45ea6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="45ea6-109">EXAMPLES</span></span>

## <span data-ttu-id="45ea6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45ea6-110">PARAMETERS</span></span>

### <span data-ttu-id="45ea6-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="45ea6-111">-CdnEndpoint</span></span>
<span data-ttu-id="45ea6-112">A parancsmag által eltávolított végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="45ea6-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45ea6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ea6-113">-DefaultProfile</span></span>
<span data-ttu-id="45ea6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="45ea6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45ea6-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="45ea6-115">-EndpointName</span></span>
<span data-ttu-id="45ea6-116">A parancsmag által eltávolított végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45ea6-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ea6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="45ea6-117">-Force</span></span>
<span data-ttu-id="45ea6-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="45ea6-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ea6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45ea6-119">-PassThru</span></span>
<span data-ttu-id="45ea6-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="45ea6-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="45ea6-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="45ea6-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45ea6-122">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="45ea6-122">-ProfileName</span></span>
<span data-ttu-id="45ea6-123">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="45ea6-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ea6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45ea6-124">-ResourceGroupName</span></span>
<span data-ttu-id="45ea6-125">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="45ea6-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ea6-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45ea6-126">-Confirm</span></span>
<span data-ttu-id="45ea6-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45ea6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45ea6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45ea6-128">-WhatIf</span></span>
<span data-ttu-id="45ea6-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45ea6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45ea6-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45ea6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45ea6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ea6-131">CommonParameters</span></span>
<span data-ttu-id="45ea6-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45ea6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ea6-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45ea6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ea6-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45ea6-134">INPUTS</span></span>

### <span data-ttu-id="45ea6-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="45ea6-135">PSEndpoint</span></span>
<span data-ttu-id="45ea6-136">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="45ea6-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="45ea6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45ea6-137">OUTPUTS</span></span>

### <span data-ttu-id="45ea6-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45ea6-138">System.Boolean</span></span>

## <span data-ttu-id="45ea6-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45ea6-139">NOTES</span></span>

## <span data-ttu-id="45ea6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45ea6-140">RELATED LINKS</span></span>

[<span data-ttu-id="45ea6-141">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="45ea6-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="45ea6-142">Új – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="45ea6-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="45ea6-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="45ea6-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="45ea6-144">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="45ea6-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="45ea6-145">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="45ea6-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


