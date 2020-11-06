---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: b2ebde9e6cf0e94e43d41cd75ee7ee09674fc3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501392"
---
# <span data-ttu-id="a9a03-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="a9a03-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="a9a03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9a03-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a03-103">Kiszolgáló-kezelési munkamenet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a9a03-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9a03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9a03-104">SYNTAX</span></span>

### <span data-ttu-id="a9a03-105">ByName</span><span class="sxs-lookup"><span data-stu-id="a9a03-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9a03-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="a9a03-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9a03-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9a03-107">DESCRIPTION</span></span>
<span data-ttu-id="a9a03-108">A **Remove-AzureRmServerManagementSession** parancsmag eltávolítja az Azure Server Management-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="a9a03-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="a9a03-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a9a03-109">EXAMPLES</span></span>

## <span data-ttu-id="a9a03-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9a03-110">PARAMETERS</span></span>

### <span data-ttu-id="a9a03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a03-111">-DefaultProfile</span></span>
<span data-ttu-id="a9a03-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9a03-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9a03-113">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="a9a03-113">-NodeName</span></span>
<span data-ttu-id="a9a03-114">Annak a csomópontnak a neve, amelyen a parancsmag eltávolítja a munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="a9a03-114">Specifies the name of the node on which this cmdlet removes the session.</span></span>

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

### <span data-ttu-id="a9a03-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a03-115">-ResourceGroupName</span></span>
<span data-ttu-id="a9a03-116">Annak az erőforráscsoport a neve, amelyhez a munkamenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="a9a03-116">Specifies the name of the resource group that the session belongs to.</span></span>

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

### <span data-ttu-id="a9a03-117">-Session</span><span class="sxs-lookup"><span data-stu-id="a9a03-117">-Session</span></span>
<span data-ttu-id="a9a03-118">A parancsmag által eltávolított munkamenetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9a03-118">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="a9a03-119">Ezt a paramétert használhatja a *ResourceGroupName* , az *csomópontnév* és a *munkamenet* paraméter helyett.</span><span class="sxs-lookup"><span data-stu-id="a9a03-119">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9a03-120">-Munkamenet</span><span class="sxs-lookup"><span data-stu-id="a9a03-120">-SessionName</span></span>
<span data-ttu-id="a9a03-121">Annak a munkamenetnek a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="a9a03-121">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a03-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a03-122">CommonParameters</span></span>
<span data-ttu-id="a9a03-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9a03-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a03-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9a03-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a03-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9a03-125">INPUTS</span></span>

### <span data-ttu-id="a9a03-126">Munkamenet</span><span class="sxs-lookup"><span data-stu-id="a9a03-126">Session</span></span>
<span data-ttu-id="a9a03-127">A "Session" paraméter elfogadja a "munkamenet" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a9a03-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="a9a03-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9a03-128">OUTPUTS</span></span>

## <span data-ttu-id="a9a03-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9a03-129">NOTES</span></span>

## <span data-ttu-id="a9a03-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9a03-130">RELATED LINKS</span></span>

[<span data-ttu-id="a9a03-131">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="a9a03-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="a9a03-132">Új – AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="a9a03-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)


