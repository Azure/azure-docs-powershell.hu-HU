---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299924"
---
# <span data-ttu-id="4691d-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4691d-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="4691d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4691d-102">SYNOPSIS</span></span>
<span data-ttu-id="4691d-103">Listát vagy API-kezelési szolgáltatás leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="4691d-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="4691d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4691d-104">SYNTAX</span></span>

### <span data-ttu-id="4691d-105">GetBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4691d-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4691d-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4691d-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4691d-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="4691d-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4691d-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4691d-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4691d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4691d-109">DESCRIPTION</span></span>
<span data-ttu-id="4691d-110">A **Get-AzApiManagement** parancsmag felsorolja az összes API-kezelési szolgáltatást az előfizetés vagy a megadott erőforráscsoport vagy egy bizonyos API-kezelés csoportban.</span><span class="sxs-lookup"><span data-stu-id="4691d-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="4691d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4691d-111">EXAMPLES</span></span>

### <span data-ttu-id="4691d-112">Példa 1: az API-kezelési szolgáltatások beszerzése</span><span class="sxs-lookup"><span data-stu-id="4691d-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="4691d-113">Ez a parancs az összes API-kezelési szolgáltatást beilleszti az előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="4691d-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="4691d-114">2. példa: az API-kezelési szolgáltatások beszerzése egy adott névvel</span><span class="sxs-lookup"><span data-stu-id="4691d-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="4691d-115">Ez a parancs a minden API-kezelési szolgáltatás bekerül a név mezőbe.</span><span class="sxs-lookup"><span data-stu-id="4691d-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="4691d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4691d-116">PARAMETERS</span></span>

### <span data-ttu-id="4691d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4691d-117">-DefaultProfile</span></span>
<span data-ttu-id="4691d-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4691d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4691d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4691d-119">-Name</span></span>
<span data-ttu-id="4691d-120">Az API-kezelési szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4691d-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="4691d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4691d-121">-ResourceGroupName</span></span>
<span data-ttu-id="4691d-122">Annak az erőforrás-csoportnak a nevét adja meg, amelyben a parancsmag az API-kezelési szolgáltatást kapja.</span><span class="sxs-lookup"><span data-stu-id="4691d-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="4691d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4691d-123">-ResourceId</span></span>
<span data-ttu-id="4691d-124">Az API-kezelési szolgáltatás ResourceId</span><span class="sxs-lookup"><span data-stu-id="4691d-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4691d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4691d-125">CommonParameters</span></span>
<span data-ttu-id="4691d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4691d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4691d-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4691d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4691d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4691d-128">INPUTS</span></span>

### <span data-ttu-id="4691d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4691d-129">System.String</span></span>

## <span data-ttu-id="4691d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4691d-130">OUTPUTS</span></span>

### <span data-ttu-id="4691d-131">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4691d-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="4691d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4691d-132">NOTES</span></span>

## <span data-ttu-id="4691d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4691d-133">RELATED LINKS</span></span>

[<span data-ttu-id="4691d-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4691d-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="4691d-135">Új – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4691d-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="4691d-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4691d-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="4691d-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4691d-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


