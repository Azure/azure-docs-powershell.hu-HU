---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 5d38a1104d1f2d1f569560027c540a2c8605bdae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011467"
---
# <span data-ttu-id="56ca5-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="56ca5-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="56ca5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="56ca5-103">Konfigurálható lemezkezelő set objektum létrehozása.</span><span class="sxs-lookup"><span data-stu-id="56ca5-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="56ca5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56ca5-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56ca5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="56ca5-105">DESCRIPTION</span></span>
<span data-ttu-id="56ca5-106">Konfigurálható lemezkezelő set objektum létrehozása.</span><span class="sxs-lookup"><span data-stu-id="56ca5-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="56ca5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="56ca5-107">EXAMPLES</span></span>

### <span data-ttu-id="56ca5-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="56ca5-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="56ca5-109">A kulcs-tárolóban az adott aktív kulcs segítségével hozza létre a Lemezkezelés bővítményt.</span><span class="sxs-lookup"><span data-stu-id="56ca5-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="56ca5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56ca5-110">PARAMETERS</span></span>

### <span data-ttu-id="56ca5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ca5-111">-DefaultProfile</span></span>
<span data-ttu-id="56ca5-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56ca5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56ca5-113">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="56ca5-113">-IdentityType</span></span>
<span data-ttu-id="56ca5-114">A DiskEncryptionSet által használt felügyelt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="56ca5-114">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="56ca5-115">Csak a SystemAssigned támogatott.</span><span class="sxs-lookup"><span data-stu-id="56ca5-115">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="56ca5-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="56ca5-116">-KeyUrl</span></span>
<span data-ttu-id="56ca5-117">Az aktív kulcsra mutató URL-cím a betárcsázón</span><span class="sxs-lookup"><span data-stu-id="56ca5-117">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="56ca5-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="56ca5-118">-Location</span></span>
<span data-ttu-id="56ca5-119">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="56ca5-119">Specifies a location.</span></span>

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

### <span data-ttu-id="56ca5-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="56ca5-120">-SourceVaultId</span></span>
<span data-ttu-id="56ca5-121">Az aktív kulcsot tartalmazó kulcskezelő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="56ca5-121">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="56ca5-122">-Címke</span><span class="sxs-lookup"><span data-stu-id="56ca5-122">-Tag</span></span>
<span data-ttu-id="56ca5-123">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="56ca5-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="56ca5-124">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="56ca5-124">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="56ca5-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="56ca5-125">-Confirm</span></span>
<span data-ttu-id="56ca5-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="56ca5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56ca5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56ca5-127">-WhatIf</span></span>
<span data-ttu-id="56ca5-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="56ca5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56ca5-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="56ca5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56ca5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ca5-130">CommonParameters</span></span>
<span data-ttu-id="56ca5-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56ca5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ca5-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="56ca5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ca5-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56ca5-133">INPUTS</span></span>

### <span data-ttu-id="56ca5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="56ca5-134">System.String</span></span>

### <span data-ttu-id="56ca5-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="56ca5-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="56ca5-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56ca5-136">OUTPUTS</span></span>

### <span data-ttu-id="56ca5-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="56ca5-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="56ca5-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56ca5-138">NOTES</span></span>

## <span data-ttu-id="56ca5-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56ca5-139">RELATED LINKS</span></span>
