---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
ms.openlocfilehash: 5bdd5e5d5212564afb1f9b06f220e8c452bcbbaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505756"
---
# <span data-ttu-id="fdd10-101">Get-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fdd10-101">Get-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="fdd10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdd10-102">SYNOPSIS</span></span>
<span data-ttu-id="fdd10-103">A meglévő hálózati profil legfelső szintű erőforrását kapja</span><span class="sxs-lookup"><span data-stu-id="fdd10-103">Gets an existing network profile top level resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdd10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdd10-104">SYNTAX</span></span>

### <span data-ttu-id="fdd10-105">Kibontott (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fdd10-105">NoExpand (Default)</span></span>
```
Get-AzureRmNetworkProfile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdd10-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdd10-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdd10-107">GetByResourceNameNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdd10-107">GetByResourceNameNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile [-ResourceGroupName <String>] [-Name <String>] -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdd10-108">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdd10-108">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdd10-109">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdd10-109">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdd10-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdd10-110">DESCRIPTION</span></span>
<span data-ttu-id="fdd10-111">A **Get-AzureRmNetworkProfile** parancsmag a meglévő hálózati profil legfelső szintű erőforrását kéri le.</span><span class="sxs-lookup"><span data-stu-id="fdd10-111">The **Get-AzureRmNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="fdd10-112">Példák</span><span class="sxs-lookup"><span data-stu-id="fdd10-112">EXAMPLES</span></span>

### <span data-ttu-id="fdd10-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fdd10-113">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="fdd10-114">Ezzel beolvassa a hálózati profil NP1 az erőforráscsoport rg1</span><span class="sxs-lookup"><span data-stu-id="fdd10-114">This retrieves the network profile np1 in resource group rg1</span></span>

## <span data-ttu-id="fdd10-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdd10-115">PARAMETERS</span></span>

### <span data-ttu-id="fdd10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdd10-116">-DefaultProfile</span></span>
<span data-ttu-id="fdd10-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdd10-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdd10-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="fdd10-118">-ExpandResource</span></span>
<span data-ttu-id="fdd10-119">A kibontani kívánt erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="fdd10-119">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceNameNoExpandParameterSet, GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdd10-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fdd10-120">-Name</span></span>
<span data-ttu-id="fdd10-121">A hálózati profil neve.</span><span class="sxs-lookup"><span data-stu-id="fdd10-121">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdd10-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdd10-122">-ResourceGroupName</span></span>
<span data-ttu-id="fdd10-123">A hálózati profil erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fdd10-123">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdd10-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdd10-124">-ResourceId</span></span>
<span data-ttu-id="fdd10-125">A hálózati profil Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="fdd10-125">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdd10-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdd10-126">CommonParameters</span></span>
<span data-ttu-id="fdd10-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdd10-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdd10-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdd10-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdd10-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdd10-129">INPUTS</span></span>

### <span data-ttu-id="fdd10-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fdd10-130">System.String</span></span>

## <span data-ttu-id="fdd10-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdd10-131">OUTPUTS</span></span>

### <span data-ttu-id="fdd10-132">Microsoft. Azure. commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fdd10-132">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="fdd10-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdd10-133">NOTES</span></span>

## <span data-ttu-id="fdd10-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdd10-134">RELATED LINKS</span></span>
