---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: f6e1d4d987ece31a91d119d1fe2ab781475fdc94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923594"
---
# <span data-ttu-id="8c6f3-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8c6f3-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="8c6f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6f3-103">Eltávolít egy integrációs fiók tanúsítványát egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="8c6f3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c6f3-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c6f3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c6f3-105">DESCRIPTION</span></span>
<span data-ttu-id="8c6f3-106">A **Remove-AzIntegrationAccountCertificate parancsmag** eltávolítja az integrációs fiók tanúsítványát egy erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="8c6f3-107">Adja meg az integrációs fiók nevét, az erőforráscsoport nevét és a tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="8c6f3-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8c6f3-109">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8c6f3-110">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8c6f3-111">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8c6f3-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c6f3-112">EXAMPLES</span></span>

### <span data-ttu-id="8c6f3-113">1. példa: Integrációs fiók tanúsítványának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8c6f3-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="8c6f3-114">Ez a parancs eltávolítja az IntegrationAccount31 nevű integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="8c6f3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c6f3-115">PARAMETERS</span></span>

### <span data-ttu-id="8c6f3-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="8c6f3-116">-CertificateName</span></span>
<span data-ttu-id="8c6f3-117">Egy integrációs fiók tanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="8c6f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6f3-118">-DefaultProfile</span></span>
<span data-ttu-id="8c6f3-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8c6f3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c6f3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8c6f3-120">-Force</span></span>
<span data-ttu-id="8c6f3-121">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8c6f3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8c6f3-122">-Name</span></span>
<span data-ttu-id="8c6f3-123">Egy integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c6f3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c6f3-124">-ResourceGroupName</span></span>
<span data-ttu-id="8c6f3-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8c6f3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c6f3-126">-Confirm</span></span>
<span data-ttu-id="8c6f3-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c6f3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c6f3-128">-WhatIf</span></span>
<span data-ttu-id="8c6f3-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c6f3-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c6f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6f3-131">CommonParameters</span></span>
<span data-ttu-id="8c6f3-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c6f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6f3-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c6f3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6f3-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c6f3-134">INPUTS</span></span>

### <span data-ttu-id="8c6f3-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8c6f3-135">System.String</span></span>

## <span data-ttu-id="8c6f3-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c6f3-136">OUTPUTS</span></span>

### <span data-ttu-id="8c6f3-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="8c6f3-137">System.Void</span></span>

## <span data-ttu-id="8c6f3-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c6f3-138">NOTES</span></span>

## <span data-ttu-id="8c6f3-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c6f3-139">RELATED LINKS</span></span>

[<span data-ttu-id="8c6f3-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8c6f3-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="8c6f3-141">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8c6f3-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="8c6f3-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="8c6f3-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


