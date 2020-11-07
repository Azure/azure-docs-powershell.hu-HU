---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 78fa17dee687547b617ff02dd11ecbf662e48040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672140"
---
# <span data-ttu-id="72e41-101">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="72e41-101">Remove-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="72e41-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72e41-102">SYNOPSIS</span></span>
<span data-ttu-id="72e41-103">Kiszolgáló-kezelési csomópont eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="72e41-103">Removes a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72e41-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72e41-104">SYNTAX</span></span>

### <span data-ttu-id="72e41-105">ByName</span><span class="sxs-lookup"><span data-stu-id="72e41-105">ByName</span></span>
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72e41-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="72e41-106">ByObject</span></span>
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72e41-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="72e41-107">DESCRIPTION</span></span>
<span data-ttu-id="72e41-108">A **Remove-AzureRmServerManagementNode** parancsmag eltávolítja az Azure Server Management csomópontot.</span><span class="sxs-lookup"><span data-stu-id="72e41-108">The **Remove-AzureRmServerManagementNode** cmdlet removes an Azure Server Management node.</span></span>

## <span data-ttu-id="72e41-109">Példák</span><span class="sxs-lookup"><span data-stu-id="72e41-109">EXAMPLES</span></span>

## <span data-ttu-id="72e41-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72e41-110">PARAMETERS</span></span>

### <span data-ttu-id="72e41-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e41-111">-DefaultProfile</span></span>
<span data-ttu-id="72e41-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72e41-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72e41-113">-Node</span><span class="sxs-lookup"><span data-stu-id="72e41-113">-Node</span></span>
<span data-ttu-id="72e41-114">Azt a csomópontot adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="72e41-114">Specifies the node for which this cmdlet removes.</span></span>

<span data-ttu-id="72e41-115">Ezt a paramétert a *ResourceGroupName* és a *csomópontnév* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="72e41-115">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72e41-116">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="72e41-116">-NodeName</span></span>
<span data-ttu-id="72e41-117">Annak a csomópontnak a neve, amelyhez a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="72e41-117">Specifies the name of the node for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e41-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e41-118">-ResourceGroupName</span></span>
<span data-ttu-id="72e41-119">Annak az erőforráscsoport a neve, amelyhez a csomópont tartozik.</span><span class="sxs-lookup"><span data-stu-id="72e41-119">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e41-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e41-120">CommonParameters</span></span>
<span data-ttu-id="72e41-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72e41-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e41-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e41-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e41-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72e41-123">INPUTS</span></span>

### <span data-ttu-id="72e41-124">Csomópont</span><span class="sxs-lookup"><span data-stu-id="72e41-124">Node</span></span>
<span data-ttu-id="72e41-125">A "Node" paraméter elfogadja a "csomópont" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="72e41-125">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="72e41-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72e41-126">OUTPUTS</span></span>

## <span data-ttu-id="72e41-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72e41-127">NOTES</span></span>

## <span data-ttu-id="72e41-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72e41-128">RELATED LINKS</span></span>

[<span data-ttu-id="72e41-129">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="72e41-129">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="72e41-130">Új – AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="72e41-130">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)


