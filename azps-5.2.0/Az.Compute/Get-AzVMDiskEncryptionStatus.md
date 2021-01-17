---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 4ad5ef08f9c12693a2fa4b4b372ee1320f90fb76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352902"
---
# <span data-ttu-id="d2365-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="d2365-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="d2365-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2365-102">SYNOPSIS</span></span>
<span data-ttu-id="d2365-103">A virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d2365-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="d2365-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d2365-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2365-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d2365-105">DESCRIPTION</span></span>
<span data-ttu-id="d2365-106">A **Get-AzVMDiskEncryptionStatus** parancsmag megkapja a virtuális gép titkosítási állapotát.</span><span class="sxs-lookup"><span data-stu-id="d2365-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="d2365-107">Megjeleníti az operációs rendszer titkosítási állapotát és az adatköteteket.</span><span class="sxs-lookup"><span data-stu-id="d2365-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="d2365-108">A titkosítási állapot mellett a titkosítási titkos URL-címet, a kulcstitkosítási kulcs URL-címét, a **KeyVaults** erőforrás-kódot is megjeleníti, ahol az operációs rendszer hangerejének titkosítási és kulcstitkosítási kulcsa is található.</span><span class="sxs-lookup"><span data-stu-id="d2365-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="d2365-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d2365-109">EXAMPLES</span></span>

### <span data-ttu-id="d2365-110">1. példa: Virtuális gép titkosítási állapotának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="d2365-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="d2365-111">Ez a parancs a VM001 nevű virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d2365-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="d2365-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2365-112">PARAMETERS</span></span>

### <span data-ttu-id="d2365-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2365-113">-DefaultProfile</span></span>
<span data-ttu-id="d2365-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2365-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2365-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="d2365-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="d2365-116">A bővítmény közzétevőjának neve.</span><span class="sxs-lookup"><span data-stu-id="d2365-116">The extension publisher name.</span></span> <span data-ttu-id="d2365-117">Ezt a paramétert csak a "Microsoft.Azure.Security" alapértelmezett értékének felülbírálása érdekében adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2365-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2365-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d2365-118">-ExtensionType</span></span>
<span data-ttu-id="d2365-119">A bővítmény típusa.</span><span class="sxs-lookup"><span data-stu-id="d2365-119">The extension type.</span></span> <span data-ttu-id="d2365-120">Ezt a paramétert megadva felülbírálhatja a Windows-VMs -hez használt "AzureDiskEncryption" és a Linux-alapú "AzureDiskEncryptionForLinux" alapértelmezett értékét.</span><span class="sxs-lookup"><span data-stu-id="d2365-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2365-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d2365-121">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2365-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2365-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2365-123">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2365-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d2365-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="d2365-124">-VMName</span></span>
<span data-ttu-id="d2365-125">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2365-125">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2365-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2365-126">CommonParameters</span></span>
<span data-ttu-id="d2365-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2365-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2365-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2365-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2365-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2365-129">INPUTS</span></span>

### <span data-ttu-id="d2365-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d2365-130">System.String</span></span>

## <span data-ttu-id="d2365-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2365-131">OUTPUTS</span></span>

### <span data-ttu-id="d2365-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d2365-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="d2365-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d2365-133">NOTES</span></span>

## <span data-ttu-id="d2365-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2365-134">RELATED LINKS</span></span>

[<span data-ttu-id="d2365-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d2365-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="d2365-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d2365-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


