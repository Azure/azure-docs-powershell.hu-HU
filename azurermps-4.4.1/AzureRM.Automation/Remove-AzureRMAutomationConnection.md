---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: aade8dec765a7336292e0350d098417e29d0e360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499240"
---
# <span data-ttu-id="c5795-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c5795-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="c5795-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5795-102">SYNOPSIS</span></span>
<span data-ttu-id="c5795-103">Automatizálási kapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c5795-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5795-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5795-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5795-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5795-105">DESCRIPTION</span></span>
<span data-ttu-id="c5795-106">A **Remove-AzureRmAutomationConnection** parancsmag eltávolít egy kapcsolatot az Azure Automation szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="c5795-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="c5795-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c5795-107">EXAMPLES</span></span>

### <span data-ttu-id="c5795-108">1. példa: kapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c5795-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c5795-109">Ez a parancs eltávolítja a ContosoConnection nevű tanúsítványt a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="c5795-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c5795-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5795-110">PARAMETERS</span></span>

### <span data-ttu-id="c5795-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c5795-111">-AutomationAccountName</span></span>
<span data-ttu-id="c5795-112">Annak az automatizálási fióknak a neve, amelyhez a parancsmag eltávolítja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="c5795-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5795-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c5795-113">-Force</span></span>
<span data-ttu-id="c5795-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="c5795-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5795-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5795-115">-Name</span></span>
<span data-ttu-id="c5795-116">Annak a kapcsolatnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="c5795-116">Specifies the name of the connection that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5795-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5795-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5795-118">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag eltávolítja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="c5795-118">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5795-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c5795-119">-Confirm</span></span>
<span data-ttu-id="c5795-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5795-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5795-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5795-121">-WhatIf</span></span>
<span data-ttu-id="c5795-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c5795-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5795-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5795-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5795-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5795-124">-DefaultProfile</span></span>
<span data-ttu-id="c5795-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5795-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5795-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5795-126">CommonParameters</span></span>
<span data-ttu-id="c5795-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5795-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5795-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5795-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5795-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5795-129">INPUTS</span></span>

## <span data-ttu-id="c5795-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5795-130">OUTPUTS</span></span>

## <span data-ttu-id="c5795-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5795-131">NOTES</span></span>

## <span data-ttu-id="c5795-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5795-132">RELATED LINKS</span></span>

[<span data-ttu-id="c5795-133">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c5795-133">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="c5795-134">Új – AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c5795-134">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


