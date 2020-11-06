---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 7d8b2e02e5683f58eee06de1993f6ea0d4ecfac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492183"
---
# <span data-ttu-id="ffe9e-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="ffe9e-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="ffe9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffe9e-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe9e-103">Kiszolgáló-kezelési munkamenet létrehozása</span><span class="sxs-lookup"><span data-stu-id="ffe9e-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffe9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffe9e-104">SYNTAX</span></span>

### <span data-ttu-id="ffe9e-105">ByName</span><span class="sxs-lookup"><span data-stu-id="ffe9e-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffe9e-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="ffe9e-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffe9e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffe9e-107">DESCRIPTION</span></span>
<span data-ttu-id="ffe9e-108">A **New-AzureRmServerManagementSession** parancsmag Azure Server Management-munkamenetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ffe9e-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="ffe9e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ffe9e-109">EXAMPLES</span></span>

## <span data-ttu-id="ffe9e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffe9e-110">PARAMETERS</span></span>

### <span data-ttu-id="ffe9e-111">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="ffe9e-111">-Credential</span></span>
<span data-ttu-id="ffe9e-112">A Kiszolgálókezelő-munkamenethez kapcsolódó kapcsolat **PSCredential** -objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffe9e-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="ffe9e-113">Hitelesítőadat-objektum beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ffe9e-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="ffe9e-114">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ffe9e-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe9e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe9e-115">-DefaultProfile</span></span>
<span data-ttu-id="ffe9e-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffe9e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffe9e-117">-Node</span><span class="sxs-lookup"><span data-stu-id="ffe9e-117">-Node</span></span>
<span data-ttu-id="ffe9e-118">Azt a csomópontot adja meg, amelyre a parancsmag létrehozta a munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="ffe9e-118">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="ffe9e-119">Ezt a paramétert a *ResourceGroupName* és a *csomópontnév* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="ffe9e-119">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

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

### <span data-ttu-id="ffe9e-120">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="ffe9e-120">-NodeName</span></span>
<span data-ttu-id="ffe9e-121">Annak a csomópontnak a nevét adja meg, amelyhez ez a parancsmag létrehoz egy munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="ffe9e-121">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe9e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffe9e-122">-ResourceGroupName</span></span>
<span data-ttu-id="ffe9e-123">Annak a csomópontnak az erőforrás csoportját adja meg, amelyre a parancsmag létrehozta a munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="ffe9e-123">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

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

### <span data-ttu-id="ffe9e-124">-Munkamenet</span><span class="sxs-lookup"><span data-stu-id="ffe9e-124">-SessionName</span></span>
<span data-ttu-id="ffe9e-125">Itt adhatja meg a munkamenethez használni kívánt nevet.</span><span class="sxs-lookup"><span data-stu-id="ffe9e-125">Specifies the name to use for the session.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe9e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe9e-126">CommonParameters</span></span>
<span data-ttu-id="ffe9e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffe9e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe9e-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffe9e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe9e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffe9e-129">INPUTS</span></span>

### <span data-ttu-id="ffe9e-130">Csomópont</span><span class="sxs-lookup"><span data-stu-id="ffe9e-130">Node</span></span>
<span data-ttu-id="ffe9e-131">A "Node" paraméter elfogadja a "csomópont" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ffe9e-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="ffe9e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffe9e-132">OUTPUTS</span></span>

### <span data-ttu-id="ffe9e-133">Microsoft. Azure. Command. ServerManagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="ffe9e-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="ffe9e-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffe9e-134">NOTES</span></span>

## <span data-ttu-id="ffe9e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffe9e-135">RELATED LINKS</span></span>

