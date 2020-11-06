---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 3c36d0b21b1fdda1282a1184f90728e827515195
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493890"
---
# <span data-ttu-id="d7adf-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d7adf-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="d7adf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7adf-102">SYNOPSIS</span></span>
<span data-ttu-id="d7adf-103">API-kezelési naplózó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d7adf-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7adf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7adf-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7adf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7adf-105">DESCRIPTION</span></span>
<span data-ttu-id="d7adf-106">A **Remove-AzureRmApiManagementLogger** parancsmag egy Azure API-kezelési **naplózó** eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d7adf-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="d7adf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d7adf-107">EXAMPLES</span></span>

### <span data-ttu-id="d7adf-108">1. példa: naplózó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d7adf-108">Example 1: Remove a logger</span></span>
```
PS C:\>Remove-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="d7adf-109">Ez a parancs eltávolítja az azonosító Logger123 tartalmazó naplózó.</span><span class="sxs-lookup"><span data-stu-id="d7adf-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="d7adf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7adf-110">PARAMETERS</span></span>

### <span data-ttu-id="d7adf-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d7adf-111">-Context</span></span>
<span data-ttu-id="d7adf-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d7adf-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7adf-113">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="d7adf-113">-LoggerId</span></span>
<span data-ttu-id="d7adf-114">Az eltávolítandó naplózó AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7adf-114">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="d7adf-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7adf-115">-PassThru</span></span>
<span data-ttu-id="d7adf-116">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikerül vagy $False más módon.</span><span class="sxs-lookup"><span data-stu-id="d7adf-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7adf-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7adf-117">-Confirm</span></span>
<span data-ttu-id="d7adf-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7adf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7adf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7adf-119">-WhatIf</span></span>
<span data-ttu-id="d7adf-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7adf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7adf-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7adf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7adf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7adf-122">-DefaultProfile</span></span>
<span data-ttu-id="d7adf-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7adf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7adf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7adf-124">CommonParameters</span></span>
<span data-ttu-id="d7adf-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7adf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7adf-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7adf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7adf-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7adf-127">INPUTS</span></span>

## <span data-ttu-id="d7adf-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7adf-128">OUTPUTS</span></span>

### <span data-ttu-id="d7adf-129">Logikai</span><span class="sxs-lookup"><span data-stu-id="d7adf-129">Boolean</span></span>

## <span data-ttu-id="d7adf-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7adf-130">NOTES</span></span>

## <span data-ttu-id="d7adf-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7adf-131">RELATED LINKS</span></span>

[<span data-ttu-id="d7adf-132">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d7adf-132">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="d7adf-133">Új – AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d7adf-133">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="d7adf-134">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d7adf-134">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


