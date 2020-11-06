---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 5a46e75f7ce7b0639de015de975c321c9d5c1ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492612"
---
# <span data-ttu-id="096f5-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="096f5-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="096f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="096f5-102">SYNOPSIS</span></span>
<span data-ttu-id="096f5-103">Egy API-kezelési szolgáltatás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="096f5-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="096f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="096f5-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="096f5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="096f5-105">DESCRIPTION</span></span>
<span data-ttu-id="096f5-106">A **Remove-AzureRmApiManagement** parancsmag eltávolítja az Azure API-kezelési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="096f5-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="096f5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="096f5-107">EXAMPLES</span></span>

### <span data-ttu-id="096f5-108">1. példa: API-kezelési szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="096f5-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="096f5-109">Ez a parancs eltávolítja a ContosoApi nevű API-kezelési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="096f5-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="096f5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="096f5-110">PARAMETERS</span></span>

### <span data-ttu-id="096f5-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="096f5-111">-Name</span></span>
<span data-ttu-id="096f5-112">A parancsmag által eltávolított API-kezelési példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="096f5-112">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="096f5-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="096f5-113">-PassThru</span></span>
<span data-ttu-id="096f5-114">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="096f5-114">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="096f5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="096f5-115">-ResourceGroupName</span></span>
<span data-ttu-id="096f5-116">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az API-kezelési példány létezik.</span><span class="sxs-lookup"><span data-stu-id="096f5-116">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="096f5-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="096f5-117">-Confirm</span></span>
<span data-ttu-id="096f5-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="096f5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="096f5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="096f5-119">-WhatIf</span></span>
<span data-ttu-id="096f5-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="096f5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="096f5-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="096f5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="096f5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096f5-122">-DefaultProfile</span></span>
<span data-ttu-id="096f5-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="096f5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="096f5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096f5-124">CommonParameters</span></span>
<span data-ttu-id="096f5-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="096f5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096f5-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096f5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096f5-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="096f5-127">INPUTS</span></span>

## <span data-ttu-id="096f5-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="096f5-128">OUTPUTS</span></span>

### <span data-ttu-id="096f5-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="096f5-129">System.Boolean</span></span>

## <span data-ttu-id="096f5-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="096f5-130">NOTES</span></span>

## <span data-ttu-id="096f5-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="096f5-131">RELATED LINKS</span></span>

[<span data-ttu-id="096f5-132">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="096f5-132">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="096f5-133">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="096f5-133">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="096f5-134">Új – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="096f5-134">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="096f5-135">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="096f5-135">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


