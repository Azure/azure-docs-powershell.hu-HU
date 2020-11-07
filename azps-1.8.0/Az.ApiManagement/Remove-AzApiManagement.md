---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: 73f30ef12270ce738341e71b0428befe6a3a3ba5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836973"
---
# <span data-ttu-id="4df54-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4df54-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="4df54-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4df54-102">SYNOPSIS</span></span>
<span data-ttu-id="4df54-103">Egy API-kezelési szolgáltatás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="4df54-103">Removes an API Management service.</span></span>

## <span data-ttu-id="4df54-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4df54-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4df54-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4df54-105">DESCRIPTION</span></span>
<span data-ttu-id="4df54-106">A **Remove-AzApiManagement** parancsmag eltávolítja az Azure API-kezelési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="4df54-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="4df54-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4df54-107">EXAMPLES</span></span>

### <span data-ttu-id="4df54-108">1. példa: API-kezelési szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4df54-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="4df54-109">Ez a parancs eltávolítja a ContosoApi nevű API-kezelési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="4df54-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="4df54-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4df54-110">PARAMETERS</span></span>

### <span data-ttu-id="4df54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df54-111">-DefaultProfile</span></span>
<span data-ttu-id="4df54-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4df54-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4df54-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4df54-113">-Name</span></span>
<span data-ttu-id="4df54-114">A parancsmag által eltávolított API-kezelési példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4df54-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4df54-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4df54-115">-PassThru</span></span>
<span data-ttu-id="4df54-116">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="4df54-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df54-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df54-117">-ResourceGroupName</span></span>
<span data-ttu-id="4df54-118">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az API-kezelési példány létezik.</span><span class="sxs-lookup"><span data-stu-id="4df54-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="4df54-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4df54-119">-Confirm</span></span>
<span data-ttu-id="4df54-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4df54-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df54-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4df54-121">-WhatIf</span></span>
<span data-ttu-id="4df54-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4df54-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4df54-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4df54-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df54-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df54-124">CommonParameters</span></span>
<span data-ttu-id="4df54-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4df54-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df54-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4df54-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df54-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4df54-127">INPUTS</span></span>

### <span data-ttu-id="4df54-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4df54-128">System.String</span></span>

## <span data-ttu-id="4df54-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4df54-129">OUTPUTS</span></span>

### <span data-ttu-id="4df54-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4df54-130">System.Boolean</span></span>

## <span data-ttu-id="4df54-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4df54-131">NOTES</span></span>

## <span data-ttu-id="4df54-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4df54-132">RELATED LINKS</span></span>

[<span data-ttu-id="4df54-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4df54-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="4df54-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4df54-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="4df54-135">Új – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4df54-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="4df54-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4df54-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


