---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 04aa8bfff795bc98b4458acb18f23535ce8bb024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496023"
---
# <span data-ttu-id="5118f-101">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="5118f-101">Remove-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="5118f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5118f-102">SYNOPSIS</span></span>
<span data-ttu-id="5118f-103">Egy erőforrás-csoportból eltávolítja az integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="5118f-103">Removes an integration account certificate from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5118f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5118f-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String>
 -CertificateName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5118f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5118f-105">DESCRIPTION</span></span>
<span data-ttu-id="5118f-106">A **Remove-AzureRmIntegrationAccountCertificate** parancsmag egy erőforrás-csoportból távolítja el az integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="5118f-106">The **Remove-AzureRmIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="5118f-107">Adja meg az integrációs fiók nevét, az erőforrás-csoport nevét és a tanúsítvány nevét.</span><span class="sxs-lookup"><span data-stu-id="5118f-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="5118f-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="5118f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5118f-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="5118f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5118f-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="5118f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5118f-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="5118f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5118f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="5118f-112">EXAMPLES</span></span>

### <span data-ttu-id="5118f-113">1. példa: az integrációs fiók tanúsítványának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5118f-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="5118f-114">Ez a parancs eltávolítja a IntegrationAccount31 nevű integrációs fiók tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="5118f-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="5118f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5118f-115">PARAMETERS</span></span>

### <span data-ttu-id="5118f-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="5118f-116">-CertificateName</span></span>
<span data-ttu-id="5118f-117">Az integrációs fiók tanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5118f-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="5118f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5118f-118">-DefaultProfile</span></span>
<span data-ttu-id="5118f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5118f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5118f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5118f-120">-Force</span></span>
<span data-ttu-id="5118f-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="5118f-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5118f-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5118f-122">-Name</span></span>
<span data-ttu-id="5118f-123">Az integrációs fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5118f-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="5118f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5118f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5118f-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5118f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5118f-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5118f-126">-Confirm</span></span>
<span data-ttu-id="5118f-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5118f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5118f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5118f-128">-WhatIf</span></span>
<span data-ttu-id="5118f-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5118f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5118f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5118f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5118f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5118f-131">CommonParameters</span></span>
<span data-ttu-id="5118f-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5118f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5118f-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5118f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5118f-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5118f-134">INPUTS</span></span>

### <span data-ttu-id="5118f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5118f-135">System.String</span></span>

## <span data-ttu-id="5118f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5118f-136">OUTPUTS</span></span>

### <span data-ttu-id="5118f-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="5118f-137">System.Void</span></span>

## <span data-ttu-id="5118f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5118f-138">NOTES</span></span>

## <span data-ttu-id="5118f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5118f-139">RELATED LINKS</span></span>

[<span data-ttu-id="5118f-140">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="5118f-140">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="5118f-141">Új – AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="5118f-141">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="5118f-142">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="5118f-142">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


