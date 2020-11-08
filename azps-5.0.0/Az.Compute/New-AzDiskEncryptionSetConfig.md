---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: bfcb306b12c047c9207e0ef2f1d82bf6eaffc4d3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186246"
---
# <span data-ttu-id="3d696-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="3d696-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="3d696-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d696-102">SYNOPSIS</span></span>
<span data-ttu-id="3d696-103">Konfigurálható lemezkezelő set objektum létrehozása.</span><span class="sxs-lookup"><span data-stu-id="3d696-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="3d696-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d696-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d696-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d696-105">DESCRIPTION</span></span>
<span data-ttu-id="3d696-106">Konfigurálható lemezkezelő set objektum létrehozása.</span><span class="sxs-lookup"><span data-stu-id="3d696-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="3d696-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3d696-107">EXAMPLES</span></span>

### <span data-ttu-id="3d696-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3d696-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="3d696-109">A kulcs-tárolóban az adott aktív kulcs segítségével hozza létre a Lemezkezelés bővítményt.</span><span class="sxs-lookup"><span data-stu-id="3d696-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="3d696-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d696-110">PARAMETERS</span></span>

### <span data-ttu-id="3d696-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d696-111">-DefaultProfile</span></span>
<span data-ttu-id="3d696-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d696-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d696-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="3d696-113">-EncryptionType</span></span>
<span data-ttu-id="3d696-114">Ezzel a beállítással megadhatja a lemez titkosítási beállításának titkosítási típusát.</span><span class="sxs-lookup"><span data-stu-id="3d696-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="3d696-115">A rendelkezésre álló értékek a következők: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey".</span><span class="sxs-lookup"><span data-stu-id="3d696-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

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

### <span data-ttu-id="3d696-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3d696-116">-IdentityType</span></span>
<span data-ttu-id="3d696-117">A DiskEncryptionSet által használt felügyelt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="3d696-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="3d696-118">Csak a SystemAssigned támogatott.</span><span class="sxs-lookup"><span data-stu-id="3d696-118">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="3d696-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="3d696-119">-KeyUrl</span></span>
<span data-ttu-id="3d696-120">Az aktív kulcsra mutató URL-cím a betárcsázón</span><span class="sxs-lookup"><span data-stu-id="3d696-120">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="3d696-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="3d696-121">-Location</span></span>
<span data-ttu-id="3d696-122">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="3d696-122">Specifies a location.</span></span>

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

### <span data-ttu-id="3d696-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="3d696-123">-SourceVaultId</span></span>
<span data-ttu-id="3d696-124">Az aktív kulcsot tartalmazó kulcskezelő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3d696-124">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d696-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="3d696-125">-Tag</span></span>
<span data-ttu-id="3d696-126">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="3d696-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3d696-127">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3d696-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d696-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d696-128">-Confirm</span></span>
<span data-ttu-id="3d696-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d696-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d696-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d696-130">-WhatIf</span></span>
<span data-ttu-id="3d696-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d696-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d696-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d696-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d696-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d696-133">CommonParameters</span></span>
<span data-ttu-id="3d696-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d696-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d696-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3d696-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d696-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d696-136">INPUTS</span></span>

### <span data-ttu-id="3d696-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3d696-137">System.String</span></span>

### <span data-ttu-id="3d696-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d696-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d696-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d696-139">OUTPUTS</span></span>

### <span data-ttu-id="3d696-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3d696-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="3d696-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d696-141">NOTES</span></span>

## <span data-ttu-id="3d696-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d696-142">RELATED LINKS</span></span>