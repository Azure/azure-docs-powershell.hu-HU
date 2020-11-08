---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183289"
---
# <span data-ttu-id="7997f-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="7997f-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="7997f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7997f-102">SYNOPSIS</span></span>
<span data-ttu-id="7997f-103">Megtudhatja, hogy milyen hozzáférési kulcsokat kell kimutatnia a jelfeldolgozó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="7997f-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="7997f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7997f-104">SYNTAX</span></span>

### <span data-ttu-id="7997f-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7997f-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7997f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7997f-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7997f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7997f-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7997f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7997f-108">DESCRIPTION</span></span>
<span data-ttu-id="7997f-109">Megtudhatja, hogy milyen hozzáférési kulcsokat kell kimutatnia a jelfeldolgozó szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="7997f-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="7997f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7997f-110">EXAMPLES</span></span>

### <span data-ttu-id="7997f-111">Adott szignáló szolgáltatáshoz tartozó hozzáférési kulcsok beszerzése</span><span class="sxs-lookup"><span data-stu-id="7997f-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="7997f-112">A Signal-szolgáltatói objektum elérési kulcsai a pipe-ban</span><span class="sxs-lookup"><span data-stu-id="7997f-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="7997f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7997f-113">PARAMETERS</span></span>

### <span data-ttu-id="7997f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7997f-114">-DefaultProfile</span></span>
<span data-ttu-id="7997f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7997f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7997f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7997f-116">-InputObject</span></span>
<span data-ttu-id="7997f-117">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="7997f-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="7997f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7997f-118">-Name</span></span>
<span data-ttu-id="7997f-119">A szignáló szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="7997f-119">SignalR service name.</span></span>

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

### <span data-ttu-id="7997f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7997f-120">-ResourceGroupName</span></span>
<span data-ttu-id="7997f-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7997f-121">Resource group name.</span></span>

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

### <span data-ttu-id="7997f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7997f-122">-ResourceId</span></span>
<span data-ttu-id="7997f-123">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7997f-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="7997f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7997f-124">CommonParameters</span></span>
<span data-ttu-id="7997f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7997f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7997f-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7997f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7997f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7997f-127">INPUTS</span></span>

### <span data-ttu-id="7997f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7997f-128">System.String</span></span>
### <span data-ttu-id="7997f-129">Microsoft. Azure. Command. Signal. models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="7997f-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="7997f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7997f-130">OUTPUTS</span></span>

### <span data-ttu-id="7997f-131">Microsoft. Azure. Command. Signal. models. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="7997f-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="7997f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7997f-132">NOTES</span></span>

## <span data-ttu-id="7997f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7997f-133">RELATED LINKS</span></span>
