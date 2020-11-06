---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: c94486e33ac39bff9d378840a6ab0ad041fa998e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493704"
---
# <span data-ttu-id="0f8dc-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="0f8dc-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="0f8dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="0f8dc-103">Beolvassa a munkaterületeket egy Power BI-munkaterületi gyűjteménybe.</span><span class="sxs-lookup"><span data-stu-id="0f8dc-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f8dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f8dc-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f8dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f8dc-105">DESCRIPTION</span></span>
<span data-ttu-id="0f8dc-106">A **Get-AzureRmPowerBIWorkspace** parancsmag a Power bi-munkaterületi gyűjteményben kapja meg a munkaterületeket.</span><span class="sxs-lookup"><span data-stu-id="0f8dc-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="0f8dc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0f8dc-107">EXAMPLES</span></span>

### <span data-ttu-id="0f8dc-108">Példa 1: munkaterület-gyűjtemény munkaterületének beszerzése</span><span class="sxs-lookup"><span data-stu-id="0f8dc-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="0f8dc-109">Ez a parancs a megadott erőforráscsoport WCN11 nevű munkaterületi gyűjteményéhez tartozó munkaterületeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0f8dc-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="0f8dc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f8dc-110">PARAMETERS</span></span>

### <span data-ttu-id="0f8dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f8dc-111">-DefaultProfile</span></span>
<span data-ttu-id="0f8dc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0f8dc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f8dc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f8dc-113">-ResourceGroupName</span></span>
<span data-ttu-id="0f8dc-114">Annak az erőforráscsoport-csoportnak a neve, amelyhez a munkaterületi gyűjtemény tartozik.</span><span class="sxs-lookup"><span data-stu-id="0f8dc-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f8dc-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0f8dc-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="0f8dc-116">Annak a munkaterületi gyűjteménynek a neve, amelyhez ez a parancsmag munkaterületet kap.</span><span class="sxs-lookup"><span data-stu-id="0f8dc-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f8dc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f8dc-117">CommonParameters</span></span>
<span data-ttu-id="0f8dc-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f8dc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f8dc-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f8dc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f8dc-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f8dc-120">INPUTS</span></span>

### <span data-ttu-id="0f8dc-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="0f8dc-121">None</span></span>
<span data-ttu-id="0f8dc-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0f8dc-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f8dc-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f8dc-123">OUTPUTS</span></span>

### <span data-ttu-id="0f8dc-124">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0f8dc-124">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="0f8dc-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f8dc-125">NOTES</span></span>

## <span data-ttu-id="0f8dc-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f8dc-126">RELATED LINKS</span></span>

[<span data-ttu-id="0f8dc-127">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0f8dc-127">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


