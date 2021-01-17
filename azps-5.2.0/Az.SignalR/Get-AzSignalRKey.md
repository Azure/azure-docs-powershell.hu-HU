---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323452"
---
# <span data-ttu-id="9b1d8-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="9b1d8-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="9b1d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b1d8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b1d8-103">Szerezze be a SignalR szolgáltatás hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="9b1d8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9b1d8-104">SYNTAX</span></span>

### <span data-ttu-id="9b1d8-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b1d8-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b1d8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b1d8-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b1d8-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b1d8-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b1d8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9b1d8-108">DESCRIPTION</span></span>
<span data-ttu-id="9b1d8-109">Szerezze be a SignalR szolgáltatás hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="9b1d8-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9b1d8-110">EXAMPLES</span></span>

### <span data-ttu-id="9b1d8-111">Adott SignalR-szolgáltatás hozzáférési kulcsának elérése</span><span class="sxs-lookup"><span data-stu-id="9b1d8-111">Get access keys of a specific SignalR service</span></span>
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

### <span data-ttu-id="9b1d8-112">Hozzáférési kulcsok be szerezni egy SignalR-szolgáltatásobjektumból a pipában</span><span class="sxs-lookup"><span data-stu-id="9b1d8-112">Get access keys from a SignalR service object in pipe</span></span>

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

## <span data-ttu-id="9b1d8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b1d8-113">PARAMETERS</span></span>

### <span data-ttu-id="9b1d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b1d8-114">-DefaultProfile</span></span>
<span data-ttu-id="9b1d8-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b1d8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b1d8-116">-InputObject</span></span>
<span data-ttu-id="9b1d8-117">A SignalR erőforrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="9b1d8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9b1d8-118">-Name</span></span>
<span data-ttu-id="9b1d8-119">SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-119">SignalR service name.</span></span>

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

### <span data-ttu-id="9b1d8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b1d8-120">-ResourceGroupName</span></span>
<span data-ttu-id="9b1d8-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-121">Resource group name.</span></span>

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

### <span data-ttu-id="9b1d8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b1d8-122">-ResourceId</span></span>
<span data-ttu-id="9b1d8-123">A SignalR szolgáltatáserőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="9b1d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b1d8-124">CommonParameters</span></span>
<span data-ttu-id="9b1d8-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b1d8-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b1d8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b1d8-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b1d8-127">INPUTS</span></span>

### <span data-ttu-id="9b1d8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9b1d8-128">System.String</span></span>
### <span data-ttu-id="9b1d8-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="9b1d8-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="9b1d8-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b1d8-130">OUTPUTS</span></span>

### <span data-ttu-id="9b1d8-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="9b1d8-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="9b1d8-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9b1d8-132">NOTES</span></span>

## <span data-ttu-id="9b1d8-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b1d8-133">RELATED LINKS</span></span>
