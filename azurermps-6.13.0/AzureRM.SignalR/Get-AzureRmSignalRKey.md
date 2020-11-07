---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
ms.openlocfilehash: 3eaef21cc9652ee7e5e4c52a51bcc3ab8bd5b1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672714"
---
# <span data-ttu-id="d2021-101">Get-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="d2021-101">Get-AzureRmSignalRKey</span></span>

## <span data-ttu-id="d2021-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2021-102">SYNOPSIS</span></span>
<span data-ttu-id="d2021-103">Megtudhatja, hogy milyen hozzáférési kulcsokat kell kimutatnia a jelfeldolgozó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="d2021-103">Get the access keys of a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2021-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2021-104">SYNTAX</span></span>

### <span data-ttu-id="d2021-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2021-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2021-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2021-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2021-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2021-107">InputObjectParameterSet</span></span>
```
Get-AzureRmSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2021-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2021-108">DESCRIPTION</span></span>
<span data-ttu-id="d2021-109">Megtudhatja, hogy milyen hozzáférési kulcsokat kell kimutatnia a jelfeldolgozó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="d2021-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="d2021-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d2021-110">EXAMPLES</span></span>

### <span data-ttu-id="d2021-111">Adott szignáló szolgáltatáshoz tartozó hozzáférési kulcsok beszerzése</span><span class="sxs-lookup"><span data-stu-id="d2021-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="d2021-112">A Signal-szolgáltatói objektum elérési kulcsai a pipe-ban</span><span class="sxs-lookup"><span data-stu-id="d2021-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzureRmSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="d2021-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2021-113">PARAMETERS</span></span>

### <span data-ttu-id="d2021-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2021-114">-DefaultProfile</span></span>
<span data-ttu-id="d2021-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2021-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2021-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2021-116">-InputObject</span></span>
<span data-ttu-id="d2021-117">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="d2021-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2021-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d2021-118">-Name</span></span>
<span data-ttu-id="d2021-119">A szignáló szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="d2021-119">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2021-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2021-120">-ResourceGroupName</span></span>
<span data-ttu-id="d2021-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d2021-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2021-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2021-122">-ResourceId</span></span>
<span data-ttu-id="d2021-123">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d2021-123">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2021-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2021-124">CommonParameters</span></span>
<span data-ttu-id="d2021-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2021-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2021-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2021-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2021-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2021-127">INPUTS</span></span>

### <span data-ttu-id="d2021-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d2021-128">System.String</span></span>
<span data-ttu-id="d2021-129">Paraméterek: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d2021-129">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="d2021-130">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d2021-130">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="d2021-131">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d2021-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d2021-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2021-132">OUTPUTS</span></span>

### <span data-ttu-id="d2021-133">Microsoft. Azure. Command. Signal. models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="d2021-133">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="d2021-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2021-134">NOTES</span></span>

## <span data-ttu-id="d2021-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2021-135">RELATED LINKS</span></span>
