---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: c636da952c02b4f2b4795cd1703c276a23a8221c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665702"
---
# <span data-ttu-id="b84d9-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b84d9-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="b84d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b84d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b84d9-103">Listát vagy API-kezelési szolgáltatás leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="b84d9-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="b84d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b84d9-104">SYNTAX</span></span>

### <span data-ttu-id="b84d9-105">GetBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b84d9-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b84d9-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b84d9-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b84d9-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="b84d9-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b84d9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b84d9-108">DESCRIPTION</span></span>
<span data-ttu-id="b84d9-109">A **Get-AzApiManagement** parancsmag felsorolja az összes API-kezelési szolgáltatást az előfizetés vagy a megadott erőforráscsoport vagy egy bizonyos API-kezelés csoportban.</span><span class="sxs-lookup"><span data-stu-id="b84d9-109">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="b84d9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b84d9-110">EXAMPLES</span></span>

### <span data-ttu-id="b84d9-111">Példa 1: az API-kezelési szolgáltatások beszerzése</span><span class="sxs-lookup"><span data-stu-id="b84d9-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="b84d9-112">Ez a parancs az összes API-kezelési szolgáltatást beilleszti az előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="b84d9-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="b84d9-113">2. példa: az API-kezelési szolgáltatások beszerzése egy adott névvel</span><span class="sxs-lookup"><span data-stu-id="b84d9-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="b84d9-114">Ez a parancs a minden API-kezelési szolgáltatás bekerül a név mezőbe.</span><span class="sxs-lookup"><span data-stu-id="b84d9-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="b84d9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b84d9-115">PARAMETERS</span></span>

### <span data-ttu-id="b84d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b84d9-116">-DefaultProfile</span></span>
<span data-ttu-id="b84d9-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b84d9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84d9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b84d9-118">-Name</span></span>
<span data-ttu-id="b84d9-119">Az API-kezelési szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b84d9-119">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b84d9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b84d9-120">-ResourceGroupName</span></span>
<span data-ttu-id="b84d9-121">Annak az erőforrás-csoportnak a nevét adja meg, amelyben a parancsmag az API-kezelési szolgáltatást kapja.</span><span class="sxs-lookup"><span data-stu-id="b84d9-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b84d9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b84d9-122">CommonParameters</span></span>
<span data-ttu-id="b84d9-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b84d9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b84d9-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b84d9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b84d9-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b84d9-125">INPUTS</span></span>

### <span data-ttu-id="b84d9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b84d9-126">System.String</span></span>

## <span data-ttu-id="b84d9-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b84d9-127">OUTPUTS</span></span>

### <span data-ttu-id="b84d9-128">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b84d9-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b84d9-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b84d9-129">NOTES</span></span>

## <span data-ttu-id="b84d9-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b84d9-130">RELATED LINKS</span></span>

[<span data-ttu-id="b84d9-131">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b84d9-131">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="b84d9-132">Új – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b84d9-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="b84d9-133">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b84d9-133">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="b84d9-134">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b84d9-134">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


