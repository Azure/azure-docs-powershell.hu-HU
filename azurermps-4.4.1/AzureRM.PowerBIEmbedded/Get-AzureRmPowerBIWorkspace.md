---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: c7beab54a416809a3f5edd033d4c7946a16b807b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504035"
---
# <span data-ttu-id="5d97c-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d97c-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="5d97c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d97c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d97c-103">Beolvassa a munkaterületeket egy Power BI-munkaterületi gyűjteménybe.</span><span class="sxs-lookup"><span data-stu-id="5d97c-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d97c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d97c-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d97c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d97c-105">DESCRIPTION</span></span>
<span data-ttu-id="5d97c-106">A **Get-AzureRmPowerBIWorkspace** parancsmag a Power bi-munkaterületi gyűjteményben kapja meg a munkaterületeket.</span><span class="sxs-lookup"><span data-stu-id="5d97c-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="5d97c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5d97c-107">EXAMPLES</span></span>

### <span data-ttu-id="5d97c-108">Példa 1: munkaterület-gyűjtemény munkaterületének beszerzése</span><span class="sxs-lookup"><span data-stu-id="5d97c-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="5d97c-109">Ez a parancs a megadott erőforráscsoport WCN11 nevű munkaterületi gyűjteményéhez tartozó munkaterületeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5d97c-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="5d97c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d97c-110">PARAMETERS</span></span>

### <span data-ttu-id="5d97c-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d97c-111">-ResourceGroupName</span></span>
<span data-ttu-id="5d97c-112">Annak az erőforráscsoport-csoportnak a neve, amelyhez a munkaterületi gyűjtemény tartozik.</span><span class="sxs-lookup"><span data-stu-id="5d97c-112">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d97c-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="5d97c-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="5d97c-114">Annak a munkaterületi gyűjteménynek a neve, amelyhez ez a parancsmag munkaterületet kap.</span><span class="sxs-lookup"><span data-stu-id="5d97c-114">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d97c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d97c-115">-DefaultProfile</span></span>
<span data-ttu-id="5d97c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d97c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d97c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d97c-117">CommonParameters</span></span>
<span data-ttu-id="5d97c-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d97c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d97c-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d97c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d97c-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d97c-120">INPUTS</span></span>

## <span data-ttu-id="5d97c-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d97c-121">OUTPUTS</span></span>

### <span data-ttu-id="5d97c-122">Microsoft. Azure. Command. Management. PowerBIEmbedded. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d97c-122">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="5d97c-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d97c-123">NOTES</span></span>

## <span data-ttu-id="5d97c-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d97c-124">RELATED LINKS</span></span>

[<span data-ttu-id="5d97c-125">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="5d97c-125">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


