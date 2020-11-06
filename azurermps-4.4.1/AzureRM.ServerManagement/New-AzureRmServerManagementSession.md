---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 0ae3e221ee39a00381f009f45a9a2f508a552b6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494694"
---
# <span data-ttu-id="fe0fd-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="fe0fd-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="fe0fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe0fd-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0fd-103">Kiszolgáló-kezelési munkamenet létrehozása</span><span class="sxs-lookup"><span data-stu-id="fe0fd-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe0fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe0fd-104">SYNTAX</span></span>

### <span data-ttu-id="fe0fd-105">ByName</span><span class="sxs-lookup"><span data-stu-id="fe0fd-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe0fd-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="fe0fd-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe0fd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe0fd-107">DESCRIPTION</span></span>
<span data-ttu-id="fe0fd-108">A **New-AzureRmServerManagementSession** parancsmag Azure Server Management-munkamenetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="fe0fd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fe0fd-109">EXAMPLES</span></span>

## <span data-ttu-id="fe0fd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe0fd-110">PARAMETERS</span></span>

### <span data-ttu-id="fe0fd-111">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="fe0fd-111">-Credential</span></span>
<span data-ttu-id="fe0fd-112">A Kiszolgálókezelő-munkamenethez kapcsolódó kapcsolat **PSCredential** -objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="fe0fd-113">Hitelesítőadat-objektum beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="fe0fd-114">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="fe0fd-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe0fd-115">-Node</span><span class="sxs-lookup"><span data-stu-id="fe0fd-115">-Node</span></span>
<span data-ttu-id="fe0fd-116">Azt a csomópontot adja meg, amelyre a parancsmag létrehozta a munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-116">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="fe0fd-117">Ezt a paramétert a *ResourceGroupName* és a *csomópontnév* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-117">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe0fd-118">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="fe0fd-118">-NodeName</span></span>
<span data-ttu-id="fe0fd-119">Annak a csomópontnak a nevét adja meg, amelyhez ez a parancsmag létrehoz egy munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-119">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe0fd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe0fd-120">-ResourceGroupName</span></span>
<span data-ttu-id="fe0fd-121">Annak a csomópontnak az erőforrás csoportját adja meg, amelyre a parancsmag létrehozta a munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-121">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe0fd-122">-Munkamenet</span><span class="sxs-lookup"><span data-stu-id="fe0fd-122">-SessionName</span></span>
<span data-ttu-id="fe0fd-123">Itt adhatja meg a munkamenethez használni kívánt nevet.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-123">Specifies the name to use for the session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe0fd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0fd-124">-DefaultProfile</span></span>
<span data-ttu-id="fe0fd-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe0fd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe0fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0fd-126">CommonParameters</span></span>
<span data-ttu-id="fe0fd-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe0fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0fd-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe0fd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0fd-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe0fd-129">INPUTS</span></span>

### <span data-ttu-id="fe0fd-130">Csomópont</span><span class="sxs-lookup"><span data-stu-id="fe0fd-130">Node</span></span>
<span data-ttu-id="fe0fd-131">A "Node" paraméter elfogadja a "csomópont" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="fe0fd-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="fe0fd-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe0fd-132">OUTPUTS</span></span>

### <span data-ttu-id="fe0fd-133">Microsoft. Azure. Command. ServerManagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="fe0fd-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="fe0fd-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe0fd-134">NOTES</span></span>

## <span data-ttu-id="fe0fd-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe0fd-135">RELATED LINKS</span></span>

