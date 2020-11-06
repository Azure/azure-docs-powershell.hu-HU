---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: e77059b94f9311caf25b58f2d626f0cafc4657e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496871"
---
# <span data-ttu-id="54c4b-101">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="54c4b-101">New-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="54c4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="54c4b-103">Kiszolgáló-kezelési csomópont létrehozása</span><span class="sxs-lookup"><span data-stu-id="54c4b-103">Creates a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54c4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54c4b-104">SYNTAX</span></span>

### <span data-ttu-id="54c4b-105">ByName</span><span class="sxs-lookup"><span data-stu-id="54c4b-105">ByName</span></span>
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54c4b-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="54c4b-106">ByObject</span></span>
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54c4b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="54c4b-107">DESCRIPTION</span></span>
<span data-ttu-id="54c4b-108">A **New-AzureRmServerManagementNode** parancsmag létrehoz egy Azure Server Management csomópontot.</span><span class="sxs-lookup"><span data-stu-id="54c4b-108">The **New-AzureRmServerManagementNode** cmdlet creates an Azure Server Management node.</span></span>

## <span data-ttu-id="54c4b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="54c4b-109">EXAMPLES</span></span>

## <span data-ttu-id="54c4b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54c4b-110">PARAMETERS</span></span>

### <span data-ttu-id="54c4b-111">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="54c4b-111">-ComputerName</span></span>
<span data-ttu-id="54c4b-112">A felügyelt számítógép számítógépének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54c4b-112">Specifies the computer name of the computer that is being managed.</span></span>

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

### <span data-ttu-id="54c4b-113">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="54c4b-113">-Credential</span></span>
<span data-ttu-id="54c4b-114">A Kiszolgálókezelő csomóponthoz való kapcsolat **PSCredential** -objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="54c4b-114">Specifies a **PSCredential** object for the connection to the Server Management Node.</span></span>
<span data-ttu-id="54c4b-115">Hitelesítőadat-objektum beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="54c4b-115">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="54c4b-116">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="54c4b-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c4b-117">-Gateway</span><span class="sxs-lookup"><span data-stu-id="54c4b-117">-Gateway</span></span>
<span data-ttu-id="54c4b-118">A csomópontot kezelő átjárót adja meg.</span><span class="sxs-lookup"><span data-stu-id="54c4b-118">Specifies the gateway that manages the node.</span></span>

<span data-ttu-id="54c4b-119">Ezt a paramétert a *ResourceGroupName* , a *GatewayName* és a *hely* paraméter helyett használhatja.</span><span class="sxs-lookup"><span data-stu-id="54c4b-119">This parameter can be used instead of the *ResourceGroupName* , *GatewayName* , and *Location* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54c4b-120">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="54c4b-120">-GatewayName</span></span>
<span data-ttu-id="54c4b-121">A csomópontot elérő átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54c4b-121">Specifies the name of the gateway that accesses the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c4b-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="54c4b-122">-Location</span></span>
<span data-ttu-id="54c4b-123">Azt a helyet adja meg, ahol ez a parancsmag hozza létre a csomópontot.</span><span class="sxs-lookup"><span data-stu-id="54c4b-123">Specifies the location in which this cmdlet creates the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c4b-124">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="54c4b-124">-NodeName</span></span>
<span data-ttu-id="54c4b-125">A csomópont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54c4b-125">Specifies the name of the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c4b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c4b-126">-ResourceGroupName</span></span>
<span data-ttu-id="54c4b-127">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehozta a csomópontot.</span><span class="sxs-lookup"><span data-stu-id="54c4b-127">Specifies the name of the resource group in which this cmdlet creates the node.</span></span>

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

### <span data-ttu-id="54c4b-128">-Címkék</span><span class="sxs-lookup"><span data-stu-id="54c4b-128">-Tags</span></span>
<span data-ttu-id="54c4b-129">A címkéket kulcs-érték párokként adja meg.</span><span class="sxs-lookup"><span data-stu-id="54c4b-129">Specifies tags as key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c4b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c4b-130">-DefaultProfile</span></span>
<span data-ttu-id="54c4b-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54c4b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54c4b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c4b-132">CommonParameters</span></span>
<span data-ttu-id="54c4b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54c4b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c4b-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54c4b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c4b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54c4b-135">INPUTS</span></span>

### <span data-ttu-id="54c4b-136">Átjáró</span><span class="sxs-lookup"><span data-stu-id="54c4b-136">Gateway</span></span>
<span data-ttu-id="54c4b-137">Az "átjáró" paraméter elfogadja az "átjáró" típusú értéket a csővezetéken</span><span class="sxs-lookup"><span data-stu-id="54c4b-137">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="54c4b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54c4b-138">OUTPUTS</span></span>

### <span data-ttu-id="54c4b-139">Microsoft. Azure. Command. ServerManagement. Model. Node</span><span class="sxs-lookup"><span data-stu-id="54c4b-139">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="54c4b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54c4b-140">NOTES</span></span>

## <span data-ttu-id="54c4b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54c4b-141">RELATED LINKS</span></span>

[<span data-ttu-id="54c4b-142">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="54c4b-142">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="54c4b-143">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="54c4b-143">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


