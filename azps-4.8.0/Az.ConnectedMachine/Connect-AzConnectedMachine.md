---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025486"
---
# <span data-ttu-id="5045b-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="5045b-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="5045b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5045b-102">SYNOPSIS</span></span>
<span data-ttu-id="5045b-103">API egy új gép regisztrálásához, és ezzel egy követett erőforrás létrehozása a KARJÁN</span><span class="sxs-lookup"><span data-stu-id="5045b-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="5045b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5045b-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="5045b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5045b-105">DESCRIPTION</span></span>
<span data-ttu-id="5045b-106">API egy új gép regisztrálásához, és ezzel egy követett erőforrás létrehozása a KARJÁN</span><span class="sxs-lookup"><span data-stu-id="5045b-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="5045b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5045b-107">EXAMPLES</span></span>

### <span data-ttu-id="5045b-108">1. példa: a gép bekapcsolt bekapcsolt számítógépként</span><span class="sxs-lookup"><span data-stu-id="5045b-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
```powershell
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name linux_eastus1_1 -Location eastus

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3235e

Name             Location OSName   Status     ProvisioningState
----             -------- ------   ------     -----------------
linux_eastus1_1  eastus   linux    Connected  Succeeded
```

<span data-ttu-id="5045b-109">A bekapcsolt gép bekapcsolt számítógépként való elhelyezése</span><span class="sxs-lookup"><span data-stu-id="5045b-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="5045b-110">2. példa: távoli számítógép csatlakoztatása csatlakoztatott eszközként</span><span class="sxs-lookup"><span data-stu-id="5045b-110">Example 2: Onboards a remote machine as a connected device</span></span>
```powershell
PS C:\> $session = Connect-PSSession -ComputerName WINBOX
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-rg -Name win_eastus1_1 -Location eastus -PSSession $session

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3236a

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
win_eastus1_1  eastus   windows  Connected  Succeeded
```

<span data-ttu-id="5045b-111">Az alaplap a távoli gépet csatlakoztatott eszközként használja a PowerShell távoli verziójában.</span><span class="sxs-lookup"><span data-stu-id="5045b-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="5045b-112">Megjegyzés: ebben az időpontban csak a Windows-példány támogatott.</span><span class="sxs-lookup"><span data-stu-id="5045b-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="5045b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5045b-113">PARAMETERS</span></span>

### <span data-ttu-id="5045b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5045b-114">-DefaultProfile</span></span>
<span data-ttu-id="5045b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5045b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5045b-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="5045b-116">-Location</span></span>
<span data-ttu-id="5045b-117">A létrehozott ConnectedMachine helye.</span><span class="sxs-lookup"><span data-stu-id="5045b-117">The location for the created ConnectedMachine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5045b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5045b-118">-Name</span></span>
<span data-ttu-id="5045b-119">A géphez használni kívánt név.</span><span class="sxs-lookup"><span data-stu-id="5045b-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="5045b-120">A program alapértelmezés szerint a hostname (állomásnév) nevet használja.</span><span class="sxs-lookup"><span data-stu-id="5045b-120">The hostname is used by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5045b-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="5045b-121">-Proxy</span></span>
<span data-ttu-id="5045b-122">A használandó proxykiszolgáló URI-ja</span><span class="sxs-lookup"><span data-stu-id="5045b-122">The URI for the proxy server to use</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5045b-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="5045b-123">-PSSession</span></span>
<span data-ttu-id="5045b-124">Ha meg van adva, a gépeket az Azure-ra szolgáló parancs az egyes PSSession belül fog futni.</span><span class="sxs-lookup"><span data-stu-id="5045b-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="5045b-125">Megjegyzés: Ez a funkció csak Windowson működik most.</span><span class="sxs-lookup"><span data-stu-id="5045b-125">NOTE: This only works on Windows for now.</span></span>

```yaml
Type: System.Management.Automation.Runspaces.PSSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5045b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5045b-126">-ResourceGroupName</span></span>
<span data-ttu-id="5045b-127">Annak az erőforráscsoportnek a neve, amelyhez hozzá szeretné adni a gépet.</span><span class="sxs-lookup"><span data-stu-id="5045b-127">The name of the resource group you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5045b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5045b-128">-SubscriptionId</span></span>
<span data-ttu-id="5045b-129">Annak az előfizetésnek az azonosítója, amelyhez hozzá szeretné adni a gépet.</span><span class="sxs-lookup"><span data-stu-id="5045b-129">The ID of the subscription you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5045b-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="5045b-130">-Tag</span></span>
<span data-ttu-id="5045b-131">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="5045b-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5045b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5045b-132">CommonParameters</span></span>
<span data-ttu-id="5045b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5045b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5045b-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5045b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5045b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5045b-135">INPUTS</span></span>

## <span data-ttu-id="5045b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5045b-136">OUTPUTS</span></span>

## <span data-ttu-id="5045b-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5045b-137">NOTES</span></span>

<span data-ttu-id="5045b-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5045b-138">ALIASES</span></span>

## <span data-ttu-id="5045b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5045b-139">RELATED LINKS</span></span>

