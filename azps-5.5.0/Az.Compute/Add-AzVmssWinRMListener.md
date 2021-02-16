---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 471baa126cd58bb241fa6b8da358769d09be3f20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162314"
---
# <span data-ttu-id="8d9e9-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="8d9e9-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="8d9e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d9e9-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9e9-103">Hozzáad egy WinRM-hallgatót a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="8d9e9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d9e9-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d9e9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d9e9-105">DESCRIPTION</span></span>
<span data-ttu-id="8d9e9-106">Az **Add-AzVmssWinRMListener** parancsmag hozzáad egy Windows Remote Management (WinRM) füzetet a virtuális gép méretarány-készletéhez (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8d9e9-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8d9e9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d9e9-107">EXAMPLES</span></span>

### <span data-ttu-id="8d9e9-108">1. példa: WinRM-hallgató hozzáadása a VMSS-hez</span><span class="sxs-lookup"><span data-stu-id="8d9e9-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="8d9e9-109">Ebben a példában egy WinRM-hallgatót ad hozzá a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="8d9e9-110">Az első parancs a **New-AzVmssConfig** parancsmaggal hoz létre egy VMSS konfigurációs objektumot, és az eredményt a következő nevű változóban $VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="8d9e9-111">A második parancs hozzáadja a VMSS-hez a megadott URL-címen található tanúsítvánnyal együtt a HTTP-protokoll WinRM-jét.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="8d9e9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d9e9-112">PARAMETERS</span></span>

### <span data-ttu-id="8d9e9-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="8d9e9-113">-CertificateUrl</span></span>
<span data-ttu-id="8d9e9-114">Megadja annak a tanúsítványnak az URL-címét, amellyel új virtuális gépeket létesít.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9e9-115">-DefaultProfile</span></span>
<span data-ttu-id="8d9e9-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d9e9-117">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8d9e9-117">-Protocol</span></span>
<span data-ttu-id="8d9e9-118">A WinRM-hallgató protokollját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="8d9e9-119">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="8d9e9-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8d9e9-120">Http</span><span class="sxs-lookup"><span data-stu-id="8d9e9-120">Http</span></span>
- <span data-ttu-id="8d9e9-121">Https</span><span class="sxs-lookup"><span data-stu-id="8d9e9-121">Https</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ProtocolTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e9-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d9e9-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8d9e9-123">A VMSS-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="8d9e9-124">Az objektum létrehozásához New-AzVmssConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d9e9-125">-Confirm</span></span>
<span data-ttu-id="8d9e9-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d9e9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d9e9-127">-WhatIf</span></span>
<span data-ttu-id="8d9e9-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d9e9-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d9e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9e9-130">CommonParameters</span></span>
<span data-ttu-id="8d9e9-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d9e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9e9-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d9e9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9e9-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d9e9-133">INPUTS</span></span>

### <span data-ttu-id="8d9e9-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d9e9-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8d9e9-135">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8d9e9-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8d9e9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8d9e9-136">System.String</span></span>

## <span data-ttu-id="8d9e9-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d9e9-137">OUTPUTS</span></span>

### <span data-ttu-id="8d9e9-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d9e9-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8d9e9-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d9e9-139">NOTES</span></span>

## <span data-ttu-id="8d9e9-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d9e9-140">RELATED LINKS</span></span>

[<span data-ttu-id="8d9e9-141">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8d9e9-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


