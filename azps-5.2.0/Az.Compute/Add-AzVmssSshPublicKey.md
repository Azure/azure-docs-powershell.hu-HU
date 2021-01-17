---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 0ba5f9cd618c86eec15eb8b0a02956e5997fc627
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346337"
---
# <span data-ttu-id="930c0-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="930c0-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="930c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="930c0-102">SYNOPSIS</span></span>
<span data-ttu-id="930c0-103">Az SSH nyilvános kulcsokat ad a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="930c0-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="930c0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="930c0-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="930c0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="930c0-105">DESCRIPTION</span></span>
<span data-ttu-id="930c0-106">Az **Add-AzVmssSshPublicKey** parancsmag hozzáadja a virtuálisgép-mérethalmazhoz (VMSS) virtuális géphez való csatlakozáshoz használható nyilvános kulcsokat a Secure Shellen (SSH) keresztül.</span><span class="sxs-lookup"><span data-stu-id="930c0-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="930c0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="930c0-107">EXAMPLES</span></span>

### <span data-ttu-id="930c0-108">1. példa: SSH nyilvános kulcs hozzáadása a VMSS-hez</span><span class="sxs-lookup"><span data-stu-id="930c0-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="930c0-109">Ebben a példában egy SSH nyilvános kulcsot ad a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="930c0-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="930c0-110">Az első parancs a **New-AzVmssConfig** parancsmaggal hoz létre egy VMSS konfigurációs objektumot, és az eredményt a következő nevű változóban $VMSS.</span><span class="sxs-lookup"><span data-stu-id="930c0-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="930c0-111">A második parancs hozzáad egy SSH-kulcsot a megadott kulcsadatokkal, és a kulcsot a megadott elérési úton tárolja a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="930c0-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="930c0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="930c0-112">PARAMETERS</span></span>

### <span data-ttu-id="930c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="930c0-113">-DefaultProfile</span></span>
<span data-ttu-id="930c0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="930c0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="930c0-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="930c0-115">-KeyData</span></span>
<span data-ttu-id="930c0-116">Egy SSH RSA nyilvános kulcsra vonatkozó adatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="930c0-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="930c0-117">-Path</span><span class="sxs-lookup"><span data-stu-id="930c0-117">-Path</span></span>
<span data-ttu-id="930c0-118">Megadja egy fájl teljes elérési útját azon a virtuális gépen, ahol ez a parancsmag az SSH nyilvános kulcsot tárolja.</span><span class="sxs-lookup"><span data-stu-id="930c0-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="930c0-119">Ha a fájl már létezik, ez a parancsmag hozzáfűzi a kulcsot a fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="930c0-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="930c0-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="930c0-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="930c0-121">A VMSS-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="930c0-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="930c0-122">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="930c0-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="930c0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="930c0-123">-Confirm</span></span>
<span data-ttu-id="930c0-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="930c0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="930c0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="930c0-125">-WhatIf</span></span>
<span data-ttu-id="930c0-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="930c0-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="930c0-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="930c0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="930c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="930c0-128">CommonParameters</span></span>
<span data-ttu-id="930c0-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="930c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="930c0-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="930c0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="930c0-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="930c0-131">INPUTS</span></span>

### <span data-ttu-id="930c0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="930c0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="930c0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="930c0-133">System.String</span></span>

## <span data-ttu-id="930c0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="930c0-134">OUTPUTS</span></span>

### <span data-ttu-id="930c0-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="930c0-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="930c0-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="930c0-136">NOTES</span></span>

## <span data-ttu-id="930c0-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="930c0-137">RELATED LINKS</span></span>

[<span data-ttu-id="930c0-138">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="930c0-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
