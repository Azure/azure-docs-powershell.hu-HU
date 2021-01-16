---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355853"
---
# <span data-ttu-id="cf444-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="cf444-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="cf444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf444-102">SYNOPSIS</span></span>
<span data-ttu-id="cf444-103">A társviszonyok regisztrált előtagját kapja meg vagy sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="cf444-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="cf444-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cf444-104">SYNTAX</span></span>

### <span data-ttu-id="cf444-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf444-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf444-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cf444-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf444-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf444-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf444-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cf444-108">DESCRIPTION</span></span>
<span data-ttu-id="cf444-109">A társviszonyok regisztrált előtagját kapja meg vagy sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="cf444-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="cf444-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cf444-110">EXAMPLES</span></span>

### <span data-ttu-id="cf444-111">Regisztrált ASN-ek listája társviszonyhoz</span><span class="sxs-lookup"><span data-stu-id="cf444-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="cf444-112">A regisztrált asn listák.</span><span class="sxs-lookup"><span data-stu-id="cf444-112">Lists registered asn.</span></span>

### <span data-ttu-id="cf444-113">Név szerint regisztrált ASN-t kap a társviszonyhoz</span><span class="sxs-lookup"><span data-stu-id="cf444-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="cf444-114">Regisztrálja a társviszony-létesítés asn-ját.</span><span class="sxs-lookup"><span data-stu-id="cf444-114">Gets registered peering asn.</span></span>

<span data-ttu-id="cf444-115">{{ Adja meg itt a példa leírását }}</span><span class="sxs-lookup"><span data-stu-id="cf444-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="cf444-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf444-116">PARAMETERS</span></span>

### <span data-ttu-id="cf444-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf444-117">-DefaultProfile</span></span>
<span data-ttu-id="cf444-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf444-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf444-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf444-119">-InputObject</span></span>
<span data-ttu-id="cf444-120">A Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="cf444-120">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf444-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cf444-121">-Name</span></span>
<span data-ttu-id="cf444-122">Az előtag neve.</span><span class="sxs-lookup"><span data-stu-id="cf444-122">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf444-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="cf444-123">-PeeringName</span></span>
<span data-ttu-id="cf444-124">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="cf444-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf444-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf444-125">-ResourceGroupName</span></span>
<span data-ttu-id="cf444-126">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="cf444-126">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf444-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf444-127">-ResourceId</span></span>
<span data-ttu-id="cf444-128">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="cf444-128">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf444-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf444-129">CommonParameters</span></span>
<span data-ttu-id="cf444-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf444-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf444-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf444-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf444-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf444-132">INPUTS</span></span>

### <span data-ttu-id="cf444-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="cf444-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="cf444-134">System.String</span><span class="sxs-lookup"><span data-stu-id="cf444-134">System.String</span></span>

## <span data-ttu-id="cf444-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf444-135">OUTPUTS</span></span>

### <span data-ttu-id="cf444-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="cf444-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="cf444-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cf444-137">NOTES</span></span>

## <span data-ttu-id="cf444-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf444-138">RELATED LINKS</span></span>
