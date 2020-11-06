---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: 4fb4bbab5c774cacd274754a106aacfeebdb533c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504596"
---
# <span data-ttu-id="301be-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="301be-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="301be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="301be-102">SYNOPSIS</span></span>
<span data-ttu-id="301be-103">Automatizálási kapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="301be-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="301be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="301be-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="301be-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="301be-105">DESCRIPTION</span></span>
<span data-ttu-id="301be-106">A **Remove-AzureRmAutomationConnection** parancsmag eltávolít egy kapcsolatot az Azure Automation szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="301be-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="301be-107">Példák</span><span class="sxs-lookup"><span data-stu-id="301be-107">EXAMPLES</span></span>

### <span data-ttu-id="301be-108">1. példa: kapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="301be-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="301be-109">Ez a parancs eltávolítja a ContosoConnection nevű tanúsítványt a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="301be-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="301be-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="301be-110">PARAMETERS</span></span>

### <span data-ttu-id="301be-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="301be-111">-AutomationAccountName</span></span>
<span data-ttu-id="301be-112">Annak az automatizálási fióknak a neve, amelyhez a parancsmag eltávolítja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="301be-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301be-113">-DefaultProfile</span></span>
<span data-ttu-id="301be-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="301be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="301be-115">-Force</span><span class="sxs-lookup"><span data-stu-id="301be-115">-Force</span></span>
<span data-ttu-id="301be-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="301be-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301be-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="301be-117">-Name</span></span>
<span data-ttu-id="301be-118">Annak a kapcsolatnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="301be-118">Specifies the name of the connection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301be-119">-ResourceGroupName</span></span>
<span data-ttu-id="301be-120">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag eltávolítja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="301be-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301be-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="301be-121">-Confirm</span></span>
<span data-ttu-id="301be-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="301be-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301be-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301be-123">-WhatIf</span></span>
<span data-ttu-id="301be-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="301be-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="301be-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="301be-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301be-126">CommonParameters</span></span>
<span data-ttu-id="301be-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="301be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301be-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="301be-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301be-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="301be-129">INPUTS</span></span>

### <span data-ttu-id="301be-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="301be-130">None</span></span>
<span data-ttu-id="301be-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="301be-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="301be-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="301be-132">OUTPUTS</span></span>

## <span data-ttu-id="301be-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="301be-133">NOTES</span></span>

## <span data-ttu-id="301be-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="301be-134">RELATED LINKS</span></span>

[<span data-ttu-id="301be-135">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="301be-135">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="301be-136">Új – AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="301be-136">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


