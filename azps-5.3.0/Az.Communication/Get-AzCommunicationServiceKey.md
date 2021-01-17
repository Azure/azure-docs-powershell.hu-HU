---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: e4a16b69e5919684b40d5b9f7fd4e97465d3565e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477910"
---
# <span data-ttu-id="316a4-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="316a4-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="316a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="316a4-102">SYNOPSIS</span></span>
<span data-ttu-id="316a4-103">Szerezze be a CommunicationService erőforrás hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="316a4-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="316a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="316a4-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="316a4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="316a4-105">DESCRIPTION</span></span>
<span data-ttu-id="316a4-106">Szerezze be a CommunicationService erőforrás hozzáférési kulcsait.</span><span class="sxs-lookup"><span data-stu-id="316a4-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="316a4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="316a4-107">EXAMPLES</span></span>

### <span data-ttu-id="316a4-108">1. példa: A megadott kommunikációs szolgáltatás kulcsának lehívása</span><span class="sxs-lookup"><span data-stu-id="316a4-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="316a4-109">Megjeleníti a ConnectionString és a key for the specified Communcation service.</span><span class="sxs-lookup"><span data-stu-id="316a4-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="316a4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="316a4-110">PARAMETERS</span></span>

### <span data-ttu-id="316a4-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="316a4-111">-CommunicationServiceName</span></span>
<span data-ttu-id="316a4-112">A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="316a4-112">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316a4-113">-DefaultProfile</span></span>
<span data-ttu-id="316a4-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="316a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316a4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="316a4-115">-ResourceGroupName</span></span>
<span data-ttu-id="316a4-116">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="316a4-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="316a4-117">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="316a4-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316a4-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="316a4-118">-SubscriptionId</span></span>
<span data-ttu-id="316a4-119">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="316a4-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="316a4-120">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="316a4-120">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316a4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="316a4-121">-Confirm</span></span>
<span data-ttu-id="316a4-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="316a4-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316a4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="316a4-123">-WhatIf</span></span>
<span data-ttu-id="316a4-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="316a4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="316a4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="316a4-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316a4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316a4-126">CommonParameters</span></span>
<span data-ttu-id="316a4-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="316a4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316a4-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="316a4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316a4-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="316a4-129">INPUTS</span></span>

## <span data-ttu-id="316a4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="316a4-130">OUTPUTS</span></span>

### <span data-ttu-id="316a4-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="316a4-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="316a4-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="316a4-132">NOTES</span></span>

<span data-ttu-id="316a4-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="316a4-133">ALIASES</span></span>

## <span data-ttu-id="316a4-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="316a4-134">RELATED LINKS</span></span>

