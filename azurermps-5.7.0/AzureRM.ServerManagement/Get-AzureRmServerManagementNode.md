---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4EE30890-B09B-4811-88AD-4BF4FD47E431
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
ms.openlocfilehash: f33c6b4c7ac1fc0f1b7de11afc8395232c599539
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494358"
---
# <span data-ttu-id="23845-101">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="23845-101">Get-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="23845-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23845-102">SYNOPSIS</span></span>
<span data-ttu-id="23845-103">Egy vagy több kiszolgálói felügyeleti csomópontot kap.</span><span class="sxs-lookup"><span data-stu-id="23845-103">Gets one or more Server Management nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23845-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23845-104">SYNTAX</span></span>

### <span data-ttu-id="23845-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="23845-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementNode [[-ResourceGroupName] <String>] [[-NodeName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23845-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="23845-106">ByNode</span></span>
```
Get-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23845-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="23845-107">DESCRIPTION</span></span>
<span data-ttu-id="23845-108">A **Get-AzureRmServerManagementNode** parancsmag egy vagy több Azure Server Management csomópontot kap.</span><span class="sxs-lookup"><span data-stu-id="23845-108">The **Get-AzureRmServerManagementNode** cmdlet gets one or more Azure Server Management nodes.</span></span>

## <span data-ttu-id="23845-109">Példák</span><span class="sxs-lookup"><span data-stu-id="23845-109">EXAMPLES</span></span>

## <span data-ttu-id="23845-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23845-110">PARAMETERS</span></span>

### <span data-ttu-id="23845-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23845-111">-DefaultProfile</span></span>
<span data-ttu-id="23845-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23845-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23845-113">-Node</span><span class="sxs-lookup"><span data-stu-id="23845-113">-Node</span></span>
<span data-ttu-id="23845-114">Azt a meglévő csomópontot adja meg, amelyből a *ResourceGroupName* és a *csomópontnév* paramétereit beolvashatja.</span><span class="sxs-lookup"><span data-stu-id="23845-114">Specifies an existing node from which to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>

```yaml
Type: Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23845-115">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="23845-115">-NodeName</span></span>
<span data-ttu-id="23845-116">Annak a csomópontnak a nevét adja meg, amelyhez a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="23845-116">Specifies the name of the node for which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23845-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23845-117">-ResourceGroupName</span></span>
<span data-ttu-id="23845-118">Annak az erőforrás csoportnak a nevét adja meg, amelyben a csomópontok tartoznak.</span><span class="sxs-lookup"><span data-stu-id="23845-118">Specifies the name of the resource group in which the nodes belong to.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23845-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23845-119">CommonParameters</span></span>
<span data-ttu-id="23845-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23845-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23845-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23845-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23845-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23845-122">INPUTS</span></span>

### <span data-ttu-id="23845-123">Csomópont</span><span class="sxs-lookup"><span data-stu-id="23845-123">Node</span></span>
<span data-ttu-id="23845-124">A "Node" paraméter elfogadja a "csomópont" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="23845-124">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="23845-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23845-125">OUTPUTS</span></span>

### <span data-ttu-id="23845-126">Microsoft. Azure. Command. ServerManagement. Model. Node</span><span class="sxs-lookup"><span data-stu-id="23845-126">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="23845-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23845-127">NOTES</span></span>

## <span data-ttu-id="23845-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23845-128">RELATED LINKS</span></span>

[<span data-ttu-id="23845-129">Új – AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="23845-129">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)

[<span data-ttu-id="23845-130">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="23845-130">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


