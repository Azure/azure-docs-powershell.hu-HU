---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 610f8589dbb6c01cae1a3eb37f886425a3664929
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492624"
---
# <span data-ttu-id="6457e-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="6457e-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="6457e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6457e-102">SYNOPSIS</span></span>
<span data-ttu-id="6457e-103">Listát vagy API-kezelési szolgáltatás leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="6457e-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6457e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6457e-104">SYNTAX</span></span>

### <span data-ttu-id="6457e-105">All in előfizetés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6457e-105">All In Subscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6457e-106">Minden az erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="6457e-106">All In Resource Group</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6457e-107">Adott API-kezelési szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="6457e-107">Specific API Management Service</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6457e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6457e-108">DESCRIPTION</span></span>
<span data-ttu-id="6457e-109">A **Get-AzureRmApiManagement** parancsmag felsorolja az összes API-kezelési szolgáltatást az előfizetés vagy a megadott erőforráscsoport vagy egy bizonyos API-kezelés csoportban.</span><span class="sxs-lookup"><span data-stu-id="6457e-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="6457e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6457e-110">EXAMPLES</span></span>

### <span data-ttu-id="6457e-111">Példa 1: az API-kezelési szolgáltatások beszerzése</span><span class="sxs-lookup"><span data-stu-id="6457e-111">Example 1: Get all API Management services</span></span>
```
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="6457e-112">Ez a parancs az összes API-kezelési szolgáltatást beilleszti az előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="6457e-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="6457e-113">2. példa: az API-kezelési szolgáltatások beszerzése egy adott névvel</span><span class="sxs-lookup"><span data-stu-id="6457e-113">Example 2: Get all API Management services by a specific name</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="6457e-114">Ez a parancs a minden API-kezelési szolgáltatás bekerül a név mezőbe.</span><span class="sxs-lookup"><span data-stu-id="6457e-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="6457e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6457e-115">PARAMETERS</span></span>

### <span data-ttu-id="6457e-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6457e-116">-Name</span></span>
<span data-ttu-id="6457e-117">Az API-kezelési szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6457e-117">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6457e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6457e-118">-ResourceGroupName</span></span>
<span data-ttu-id="6457e-119">Annak az erőforrás-csoportnak a nevét adja meg, amelyben a parancsmag az API-kezelési szolgáltatást kapja.</span><span class="sxs-lookup"><span data-stu-id="6457e-119">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6457e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6457e-120">-DefaultProfile</span></span>
<span data-ttu-id="6457e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6457e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6457e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6457e-122">CommonParameters</span></span>
<span data-ttu-id="6457e-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6457e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6457e-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6457e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6457e-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6457e-125">INPUTS</span></span>

## <span data-ttu-id="6457e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6457e-126">OUTPUTS</span></span>

### <span data-ttu-id="6457e-127">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ApiManagement. models. PsApiManagement]</span><span class="sxs-lookup"><span data-stu-id="6457e-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement]</span></span>

## <span data-ttu-id="6457e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6457e-128">NOTES</span></span>

## <span data-ttu-id="6457e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6457e-129">RELATED LINKS</span></span>

[<span data-ttu-id="6457e-130">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="6457e-130">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="6457e-131">Új – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="6457e-131">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="6457e-132">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="6457e-132">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="6457e-133">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="6457e-133">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


